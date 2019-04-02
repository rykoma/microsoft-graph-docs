
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of DateTimeTimeZone
var scheduledEndDateTime = new DateTimeTimeZone
{
	DateTime = "2016-03-28T18:00:00",
	TimeZone = "UTC",
};

//create instance of DateTimeTimeZone
var scheduledStartDateTime = new DateTimeTimeZone
{
	DateTime = "2016-03-20T18:00:00",
	TimeZone = "UTC",
};

//create instance of AutomaticRepliesSetting
var automaticRepliesSetting = new AutomaticRepliesSetting
{
	Status = "Scheduled",
	ScheduledStartDateTime = scheduledStartDateTime,
	ScheduledEndDateTime = scheduledEndDateTime,
};

//create instance of MailboxSettings
var mailboxSettings = new MailboxSettings
{
	@odata.context = "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings",
	AutomaticRepliesSetting = automaticRepliesSetting,
};

await graphClient.Me.MailboxSettings
	.Request()
	.UpdateAsync(mailboxSettings);

```