
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of CalendarGroup
var calendarGroups = new CalendarGroup
{
	Name = "name-value",
};

await graphClient.Me.CalendarGroups["{id}"]
	.Request()
	.UpdateAsync(calendarGroups);

```