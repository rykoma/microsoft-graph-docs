
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = await graphClient.Me.Drive.Items["{item-id}"].Versions["{version-id}"].Content
	.Request()
	.GetAsync();

```