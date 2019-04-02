
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of OutlookTaskFolder
var taskFolders = new OutlookTaskFolder
{
	Name = "Charity work",
};

await graphClient.Me.Outlook.TaskFolders["AAMkADIyAAAhrbPWAAA="]
	.Request()
	.UpdateAsync(taskFolders);

```