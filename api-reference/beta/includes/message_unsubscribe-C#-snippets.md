
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Messages["{id}"]
	.unsubscribe();
	.Request()
	.PostAsync()

```