
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = await graphClient.Drive.Items["{item-id}"].Content
	.Request()
	.GetAsync();

```