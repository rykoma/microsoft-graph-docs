
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.unsubscribeByMail();
	.Request()
	.PostAsync()

```