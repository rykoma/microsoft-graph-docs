
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var settings = await graphClient.Settings["{id}"]
	.Request()
	.GetAsync();

```