
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"]
	.mute(clientContext);
	.Request()
	.PostAsync()

```