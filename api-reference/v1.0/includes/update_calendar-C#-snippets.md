
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Calendar
var calendar = new Calendar
{
	Name = "Social events",
};

await graphClient.Me.Calendar
	.Request()
	.UpdateAsync(calendar);

```