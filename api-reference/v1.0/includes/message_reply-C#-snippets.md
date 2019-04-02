
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

await graphClient.Me.Messages["{id}"]
	.reply(comment);
	.Request()
	.PostAsync()

```