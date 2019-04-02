
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var programControlTypes = await graphClient.ProgramControlTypes
	.Request()
	.GetAsync();

```