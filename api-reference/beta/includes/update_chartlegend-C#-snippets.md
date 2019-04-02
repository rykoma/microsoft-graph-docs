
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookChartLegend
var legend = new WorkbookChartLegend
{
	Visible = true,
	Position = "position-value",
	Overlay = true,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["name"].Legend
	.Request()
	.UpdateAsync(legend);

```