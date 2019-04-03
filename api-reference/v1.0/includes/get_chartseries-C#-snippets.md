
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var series = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Series["{series-id}"]
	.Request()
	.GetAsync();

```