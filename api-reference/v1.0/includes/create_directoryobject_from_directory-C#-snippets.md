
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Directory.DeletedItems["{object-id}"]
	.Restore()
	.Request()
	.PostAsync()

```