
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookChartTitle
var title = new WorkbookChartTitle
{
	Overlay = true,
	Text = "text-value",
	Visible = true,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["name"].Title
	.Request()
	.UpdateAsync(title);

```