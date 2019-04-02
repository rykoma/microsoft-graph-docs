
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = False;

await graphClient.Groups["{id}"]
	.getMemberObjects(securityEnabledOnly);
	.Request()
	.PostAsync()

```