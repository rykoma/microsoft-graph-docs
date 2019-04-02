
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.subscribeByMail();
	.Request()
	.PostAsync()

```