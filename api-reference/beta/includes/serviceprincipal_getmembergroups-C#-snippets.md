
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = True;

await graphClient.ServicePrincipals["{id}"]
	.getMemberGroups(securityEnabledOnly);
	.Request()
	.PostAsync()

```