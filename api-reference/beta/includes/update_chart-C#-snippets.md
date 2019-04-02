
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookChart
var charts = new WorkbookChart
{
	Height = 99,
	Left = 99,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["name"]
	.Request()
	.UpdateAsync(charts);

```