
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var signIns = await graphClient.AuditLogs.SignIns
	.Request()
	.GetAsync();

```