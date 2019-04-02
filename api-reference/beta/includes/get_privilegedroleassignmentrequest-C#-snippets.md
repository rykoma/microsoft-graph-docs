
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var privilegedRoleAssignmentRequests = await graphClient.PrivilegedRoleAssignmentRequests
	.Request()
	.GetAsync();

```