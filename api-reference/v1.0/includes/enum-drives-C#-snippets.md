
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var drives = await graphClient.Me.Drives
	.Request()
	.GetAsync();

```