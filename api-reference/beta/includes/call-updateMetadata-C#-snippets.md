
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var metadata = "metadata-value";

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"]
	.updateMetadata(metadata,clientContext);
	.Request()
	.PostAsync()

```