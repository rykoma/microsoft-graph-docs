
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFill
var fill = new WorkbookRangeFill
{
	Color = "#00FF00",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$B$1').Format.Fill
	.Request()
	.UpdateAsync(fill);

```