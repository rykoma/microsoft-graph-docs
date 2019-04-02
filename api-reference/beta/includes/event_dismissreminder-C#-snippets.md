
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Events["{id}"]
	.dismissReminder();
	.Request()
	.PostAsync()

```