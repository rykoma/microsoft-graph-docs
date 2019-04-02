
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drives["{drive-id}"].Items["{item-id}"]
	.checkout();
	.Request()
	.PostAsync()

```