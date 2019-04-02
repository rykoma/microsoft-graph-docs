
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var storageLocation = "storageLocation-value";

await graphClient.Users["{id}"]
	.exportPersonalData(storageLocation);
	.Request()
	.PostAsync()

```