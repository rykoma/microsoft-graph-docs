
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var body = new ItemBody
{
	ContentType = "html",
	Content = "this is body content",
};

var posts = new List<Post>();
posts.Add(new Post(body));

var conversationThread = new ConversationThread
{
	Topic = "topic-value",
	Posts = posts,
};

await graphClient.Groups["{id}"].Conversations["{id}"].Threads
	.Request()
	.AddAsync(conversationThread);

```