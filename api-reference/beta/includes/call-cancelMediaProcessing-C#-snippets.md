
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var all = True;

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"]
	.cancelMediaProcessing(all,clientContext);
	.Request()
	.PostAsync()

```