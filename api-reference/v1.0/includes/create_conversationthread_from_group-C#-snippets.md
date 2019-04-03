
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var emailAddress = new EmailAddress
{
	Name = "Alex Darrow",
	Address = "alexd@contoso.com",
};

var newParticipants = new List<Recipient>();
newParticipants.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "html",
	Content = "this is body content",
};

var posts = new List<Post>();
posts.Add(new Post(body,newParticipants));

var conversationThread = new ConversationThread
{
	Topic = "New Conversation Thread Topic",
	Posts = posts,
};

await graphClient.Groups["{id}"].Threads
	.Request()
	.AddAsync(conversationThread);

```