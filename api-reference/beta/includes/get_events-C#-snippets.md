
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var event = await graphClient.Me.Events
	.Request()
	.Header("Prefer","outlook.timezone="Pacific Standard Time"")
	.Select("subject,body,bodyPreview,organizer,attendees,start,end,location")
	.GetAsync();

```