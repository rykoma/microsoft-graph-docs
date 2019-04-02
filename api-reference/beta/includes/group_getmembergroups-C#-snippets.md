
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = False;

await graphClient.Groups["{id}"]
	.getMemberGroups(securityEnabledOnly);
	.Request()
	.PostAsync()

```