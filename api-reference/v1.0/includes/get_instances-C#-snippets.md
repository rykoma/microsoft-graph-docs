
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var event = await graphClient.Me.Events["AAMkAGUzYRgWAAA="].Instances
	.Request()
	.Select("subject,bodyPreview,seriesMasterId,type,recurrence,start,end")
	.GetAsync();

```