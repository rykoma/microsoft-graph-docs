
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>();

await graphClient.Contacts["{id}"]
	.CheckMemberGroups(groupIds)
	.Request()
	.PostAsync()

```