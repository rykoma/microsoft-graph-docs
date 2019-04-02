
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Education.SynchronizationProfiles["{id}"]
	.reset();
	.Request()
	.PostAsync()

```