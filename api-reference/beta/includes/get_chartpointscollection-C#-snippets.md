
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookChartPoint = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["name"].Series["undefined"].Points
	.Request()
	.GetAsync();

```