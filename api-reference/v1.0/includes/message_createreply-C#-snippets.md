
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Messages["{id}"]
	.createReply();
	.Request()
	.PostAsync()

```