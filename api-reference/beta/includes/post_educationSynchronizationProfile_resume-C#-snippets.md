
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Education.SynchronizationProfiles["{id}"]
	.resume();
	.Request()
	.PostAsync()

```