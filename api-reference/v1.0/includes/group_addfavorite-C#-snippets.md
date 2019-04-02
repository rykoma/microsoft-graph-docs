
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Groups["{id}"]
	.addFavorite();
	.Request()
	.PostAsync()

```