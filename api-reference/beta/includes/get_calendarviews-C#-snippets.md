
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var event = await graphClient.Groups["02bd9fd6-8f93-4758-87c3-1fb73740a315"].CalendarView
	.Request()
	.Header("Prefer","outlook.body-content-type="text"")
	.GetAsync();

```