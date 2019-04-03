
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>();

await graphClient.ServicePrincipals["{id}"]
	.CheckMemberGroups(groupIds)
	.Request()
	.PostAsync()

```