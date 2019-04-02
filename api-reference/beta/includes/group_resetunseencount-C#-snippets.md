
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.resetUnseenCount();
	.Request()
	.PostAsync()

```