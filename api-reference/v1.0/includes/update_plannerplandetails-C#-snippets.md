
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerCategoryDescriptions
var categoryDescriptions = new PlannerCategoryDescriptions
{
	Category1 = "Indoors",
	Category3 = null,
};

//create instance of PlannerUserIds
var sharedWith = new PlannerUserIds
{
	6463a5ce-2119-4198-9f2a-628761df4a62 = true,
	D95e6152-f683-4d78-9ff5-67ad180fea4a = false,
};

//create instance of PlannerPlanDetails
var details = new PlannerPlanDetails
{
	SharedWith = sharedWith,
	CategoryDescriptions = categoryDescriptions,
};

await graphClient.Planner.Plans["{plan-id}"].Details
	.Request()
	.UpdateAsync(details);

```