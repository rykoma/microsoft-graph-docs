
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var office365ActiveUserDetail = await graphClient.Reports.GetOffice365ActiveUserDetail('D7')
	.Request()
	.GetAsync();

```