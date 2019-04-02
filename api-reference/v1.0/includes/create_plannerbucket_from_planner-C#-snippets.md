
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of PlannerBucket
var buckets = new PlannerBucket
{
	Name = "Advertising",
	PlanId = "xqQg5FS2LkCp935s-FIFm2QAFkHM",
	OrderHint = " !",
};

await graphClient.Planner.Buckets
	.Request()
	.AddAsync(buckets);

```