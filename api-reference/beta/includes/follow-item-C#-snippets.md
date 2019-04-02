
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Items["{item-id}"]
	.follow();
	.Request()
	.PostAsync()

```