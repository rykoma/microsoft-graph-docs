
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Messages["{id}"]
	.createReplyAll();
	.Request()
	.PostAsync()

```