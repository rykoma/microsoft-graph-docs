
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var subscribedSkus = await graphClient.SubscribedSkus
	.Request()
	.GetAsync();

```