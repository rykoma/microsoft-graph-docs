
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = True;

await graphClient.ServicePrincipals["{id}"]
	.getMemberObjects(securityEnabledOnly);
	.Request()
	.PostAsync()

```