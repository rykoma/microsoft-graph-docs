
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var events = await graphClient.Me.Events["AAMkAGI1AAAoZDOFAAA="]
	.Request()
	.Header("Prefer","outlook.body-content-type="text"")
	.Select("subject,body,bodyPreview")
	.GetAsync();

```