
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.PrivilegedRoles["{id}"]
	.selfDeactivate();
	.Request()
	.PostAsync()

```