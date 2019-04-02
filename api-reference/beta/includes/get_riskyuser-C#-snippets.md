
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var riskyUsers = await graphClient.RiskyUsers["{id}"]
	.Request()
	.GetAsync();

```