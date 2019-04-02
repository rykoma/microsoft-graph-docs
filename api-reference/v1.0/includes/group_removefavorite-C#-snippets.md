
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.removeFavorite();
	.Request()
	.PostAsync()

```