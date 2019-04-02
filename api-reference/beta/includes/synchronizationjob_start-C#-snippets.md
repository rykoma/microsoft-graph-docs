
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{jobId}"]
	.start();
	.Request()
	.PostAsync()

```