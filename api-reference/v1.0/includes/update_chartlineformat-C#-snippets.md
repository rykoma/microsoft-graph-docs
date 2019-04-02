
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookChartLineFormat
var line = new WorkbookChartLineFormat
{
	Color = "color-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Axes.SeriesAxis.Format.Line
	.Request()
	.UpdateAsync(line);

```