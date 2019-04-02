
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var value = new List<String>();

await graphClient.Security.TiIndicators
	.DeleteTiIndicators(value)
	.Request()
	.PostAsync()

```