
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var threads = await graphClient.Groups["{id}"].Threads["{id}"]
	.Request()
	.GetAsync();

```