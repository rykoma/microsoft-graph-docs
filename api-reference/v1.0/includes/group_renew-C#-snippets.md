
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.renew();
	.Request()
	.PostAsync()

```