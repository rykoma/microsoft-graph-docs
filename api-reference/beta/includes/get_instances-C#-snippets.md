
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var instances = await graphClient.Me.Events["AAMkAGUzYRgWAAA="].Instances
	.Request()
	.Select("subject,bodyPreview,seriesMasterId,type,recurrence,start,end")
	.GetAsync();

```