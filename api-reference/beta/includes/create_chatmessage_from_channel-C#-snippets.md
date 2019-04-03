
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var user = new Identity
{
	DisplayName = "Jane Smith",
	Id = "ef1c916a-3135-4417-ba27-8eb7bd084193",
	UserIdentityType = "aadUser",
};

var mentioned = new IdentitySet
{
	User = user,
};

var mentionText = "Jane Smith";

var id = 0;

var mentions = new List<ChatMessageMention>();
mentions.Add(new ChatMessageMention(id,mentionText,mentioned));

var body = new ItemBody
{
	ContentType = "html",
	Content = "Hello World <at id=\"0\">Jane Smith</at>",
};

var chatMessage = new ChatMessage
{
	Body = body,
	Mentions = mentions,
};

await graphClient.Teams["{id}"].Channels["{id}"].Messages
	.Request()
	.AddAsync(chatMessage);

```