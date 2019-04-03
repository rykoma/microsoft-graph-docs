
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var dataLabels = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].DataLabels
	.Request()
	.GetAsync();

```