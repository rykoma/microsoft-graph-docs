
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ResponseStatus
var responseStatus = new ResponseStatus
{
	Response = "",
	Time = "datetime-value",
};

//create instance of ConversationThread
var threads = new ConversationThread
{
	OriginalStartTimeZone = "originalStartTimeZone-value",
	OriginalEndTimeZone = "originalEndTimeZone-value",
	ResponseStatus = responseStatus,
	ICalUId = "iCalUId-value",
	ReminderMinutesBeforeStart = 99,
	IsReminderOn = true,
};

await graphClient.Groups["02bd9fd6-8f93-4758-87c3-1fb73740a315"].Threads["AAQkAGI5MWY5ZmUyLTJiNzYtNDE0ZC04OWEwLWM3M2FjYmM3NzNlZgMkABAAG5c7eC4NYEynIoXsuxXB9RAAG5c7eC4NYEynIoXsuxXB9Q=="]
	.Request()
	.UpdateAsync(threads);

```