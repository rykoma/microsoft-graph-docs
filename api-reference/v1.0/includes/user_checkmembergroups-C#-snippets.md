
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>();

await graphClient.Me
	.CheckMemberGroups(groupIds)
	.Request()
	.PostAsync()

```