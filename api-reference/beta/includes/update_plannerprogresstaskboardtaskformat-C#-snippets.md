
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerProgressTaskBoardTaskFormat
var progressTaskBoardFormat = new PlannerProgressTaskBoardTaskFormat
{
	OrderHint = "A6673H Ejkl!",
};

await graphClient.Planner.Tasks["'id'"].ProgressTaskBoardFormat
	.Request()
	.UpdateAsync(progressTaskBoardFormat);

```