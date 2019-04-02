
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupId = "ffffffff-ffff-ffff-ffff-ffffffffffff";

await graphClient.GroupLifecyclePolicies
	.renewGroup(groupId);
	.Request()
	.PostAsync()

```