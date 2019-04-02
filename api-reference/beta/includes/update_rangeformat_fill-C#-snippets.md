
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFill
var fill = new WorkbookRangeFill
{
	Color = "#FF0000",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$A$1').Format.Fill
	.Request()
	.UpdateAsync(fill);

```