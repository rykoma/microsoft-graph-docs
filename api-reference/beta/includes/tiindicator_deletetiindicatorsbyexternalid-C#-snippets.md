
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = new List<String>();

await graphClient.Security.TiIndicators
	.DeleteTiIndicatorsByExternalId(value)
	.Request()
	.PostAsync()

```