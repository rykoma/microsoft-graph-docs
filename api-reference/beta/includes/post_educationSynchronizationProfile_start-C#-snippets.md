
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Education.SynchronizationProfiles["{id}"]
	.start();
	.Request()
	.PostAsync()

```