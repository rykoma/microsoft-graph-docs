
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = await graphClient.Me.Drive.Items["{item-id}"].Content
	.Request()
	.GetAsync();

```