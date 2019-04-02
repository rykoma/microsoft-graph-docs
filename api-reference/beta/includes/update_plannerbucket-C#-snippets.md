
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerBucket
var buckets = new PlannerBucket
{
	Name = "Development",
};

await graphClient.Planner.Buckets["hsOf2dhOJkqyYYZEtdzDe2QAIUCR"]
	.Request()
	.UpdateAsync(buckets);

```