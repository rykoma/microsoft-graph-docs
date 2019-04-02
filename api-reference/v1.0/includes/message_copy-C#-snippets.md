
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var destinationId = "destinationId-value";

await graphClient.Me.Messages["{id}"]
	.copy(destinationId);
	.Request()
	.PostAsync()

```