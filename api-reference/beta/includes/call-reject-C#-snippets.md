
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var reason = "none";

await graphClient.App.Calls["{id}"]
	.reject(reason);
	.Request()
	.PostAsync()

```