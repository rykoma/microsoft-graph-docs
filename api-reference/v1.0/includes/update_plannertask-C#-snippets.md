
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerAppliedCategories
var appliedCategories = new PlannerAppliedCategories
{
	Category3 = true,
	Category4 = false,
};

//create instance of Fbab97d0-4932-4511-b675-204639209557
var fbab97d0-4932-4511-b675-204639209557 = new Fbab97d0-4932-4511-b675-204639209557
{
	@odata.type = "#microsoft.graph.plannerAssignment",
	OrderHint = "N9917 U2883!",
};

//create instance of PlannerAssignments
var assignments = new PlannerAssignments
{
	Fbab97d0-4932-4511-b675-204639209557 = fbab97d0-4932-4511-b675-204639209557,
};

//create instance of PlannerTask
var tasks = new PlannerTask
{
	Assignments = assignments,
	AppliedCategories = appliedCategories,
};

await graphClient.Planner.Tasks["{task-id}"]
	.Request()
	.UpdateAsync(tasks);

```