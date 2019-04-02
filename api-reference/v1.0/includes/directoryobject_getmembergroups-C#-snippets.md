
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var securityEnabledOnly = True;

await graphClient.DirectoryObjects["{object-id}"]
	.getMemberGroups(securityEnabledOnly);
	.Request()
	.PostAsync()

```