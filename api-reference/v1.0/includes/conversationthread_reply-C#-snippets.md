
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ItemBody
var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

//create instance of Post
var post = new Post
{
	Body = body,
};

await graphClient.Groups["{id}"].Threads["{id}"]
	.Reply(post)
	.Request()
	.PostAsync()

```