
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerBucket
var buckets = new PlannerBucket
{
	Name = "Development",
};

await graphClient.Planner.Buckets["{bucket-id}"]
	.Request()
	.UpdateAsync(buckets);

```