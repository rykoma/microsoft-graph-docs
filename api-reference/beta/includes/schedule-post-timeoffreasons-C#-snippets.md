
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of TimeOffReason
var timeOffReasons = new TimeOffReason
{
	DisplayName = "Vacation",
	IconType = "plane",
	IsActive = true,
};

await graphClient.Teams["{teamId}"].Schedule.TimeOffReasons
	.Request()
	.AddAsync(timeOffReasons);

```