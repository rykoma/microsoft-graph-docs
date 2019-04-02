
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messages = await graphClient.Me.Messages
	.Request()
	.GetAsync();

```