
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages
	.Request()
	.GetAsync();

```