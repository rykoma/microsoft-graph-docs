
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Security.SecurityActions["{id}"]
	.cancelSecurityAction();
	.Request()
	.PostAsync()

```