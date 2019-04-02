
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var delta = await graphClient.Me.CalendarView.Delta()
	.Request()
	.GetAsync();

```