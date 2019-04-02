
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var findRooms = await graphClient.Me.FindRooms()
	.Request()
	.GetAsync();

```