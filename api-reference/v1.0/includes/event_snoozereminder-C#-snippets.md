
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of DateTimeTimeZone
var newReminderTime = new DateTimeTimeZone
{
	DateTime = "dateTime-value",
	TimeZone = "timeZone-value",
};

await graphClient.Me.Events["{id}"]
	.SnoozeReminder(newReminderTime)
	.Request()
	.PostAsync()

```