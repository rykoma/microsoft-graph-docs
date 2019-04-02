
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerBucketTaskBoardTaskFormat
var bucketTaskBoardFormat = new PlannerBucketTaskBoardTaskFormat
{
	OrderHint = "A6673H Ejkl!",
};

await graphClient.Planner.Tasks["{task-id}"].BucketTaskBoardFormat
	.Request()
	.UpdateAsync(bucketTaskBoardFormat);

```