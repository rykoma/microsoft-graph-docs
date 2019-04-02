
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = True;

await graphClient.Me
	.getMemberGroups(securityEnabledOnly);
	.Request()
	.PostAsync()

```