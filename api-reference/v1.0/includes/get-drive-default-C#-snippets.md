
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var drive = await graphClient.Me.Drive
	.Request()
	.GetAsync();

```