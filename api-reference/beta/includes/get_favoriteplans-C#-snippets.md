
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var plannerPlan = await graphClient.Me.Planner.FavoritePlans
	.Request()
	.GetAsync();

```