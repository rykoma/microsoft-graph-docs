
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var directoryObject = await graphClient.Groups["{id}"].TransitiveMemberOf
	.Request()
	.GetAsync();

```