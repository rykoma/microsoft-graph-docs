
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of OutlookTaskGroup
var taskGroups = new OutlookTaskGroup
{
	Name = "Leisure tasks",
};

await graphClient.Me.Outlook.TaskGroups
	.Request()
	.AddAsync(taskGroups);

```