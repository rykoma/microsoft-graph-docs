
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = True;

await graphClient.Me
	.getMemberObjects(securityEnabledOnly);
	.Request()
	.PostAsync()

```