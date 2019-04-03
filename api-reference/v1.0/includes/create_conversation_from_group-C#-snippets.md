
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var emailAddress = new EmailAddress
{
	Name = "Adele Vance",
	Address = "AdeleV@contoso.onmicrosoft.com",
};

var newParticipants = new List<Recipient>();
newParticipants.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "html",
	Content = "What do we know so far?",
};

var posts = new List<Post>();
posts.Add(new Post(body,newParticipants));

var threads = new List<ConversationThread>();
threads.Add(new ConversationThread(posts));

var conversation = new Conversation
{
	Topic = "New locations for this quarter",
	Threads = threads,
};

await graphClient.Groups["29981b6a-0e57-42dc-94c9-cd24f5306196"].Conversations
	.Request()
	.AddAsync(conversation);

```