
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var joinedTeams = await graphClient.Me.JoinedTeams
	.Request()
	.GetAsync();

```