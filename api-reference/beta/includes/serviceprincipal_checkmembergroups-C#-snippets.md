
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var groupIds = new List<String>();

await graphClient.ServicePrincipals["{id}"]
	.checkMemberGroups(groupIds);
	.Request()
	.PostAsync()

```