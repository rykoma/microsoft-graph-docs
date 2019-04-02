
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerOrderHintsByAssignee
var orderHintsByAssignee = new PlannerOrderHintsByAssignee
{
	Aaa27244-1db4-476a-a5cb-004607466324 = "8566473P 957764Jk!",
};

//create instance of PlannerAssignedToTaskBoardTaskFormat
var assignedToTaskBoardFormat = new PlannerAssignedToTaskBoardTaskFormat
{
	OrderHintsByAssignee = orderHintsByAssignee,
};

await graphClient.Planner.Tasks["01gzSlKkIUSUl6DF_EilrmQAKDhh"].AssignedToTaskBoardFormat
	.Request()
	.UpdateAsync(assignedToTaskBoardFormat);

```