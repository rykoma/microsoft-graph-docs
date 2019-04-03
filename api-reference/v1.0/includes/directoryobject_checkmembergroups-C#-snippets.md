
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>();

await graphClient.DirectoryObjects["{id}"]
	.CheckMemberGroups(groupIds)
	.Request()
	.PostAsync()

```