
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.PrivilegedRoleAssignments["{id}"]
	.makeEligible();
	.Request()
	.PostAsync()

```