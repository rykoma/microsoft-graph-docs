
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var userIds = new List<String>();

var schedulingGroup = new SchedulingGroup
{
	DisplayName = "Cashiers",
	IsActive = true,
	UserIds = userIds,
};

await graphClient.Teams["{teamId}"].Schedule.SchedulingGroups
	.Request()
	.AddAsync(schedulingGroup);

```