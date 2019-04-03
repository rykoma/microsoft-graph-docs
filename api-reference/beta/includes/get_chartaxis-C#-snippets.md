
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var valueAxis = await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["name"].Axes.ValueAxis
	.Request()
	.GetAsync();

```