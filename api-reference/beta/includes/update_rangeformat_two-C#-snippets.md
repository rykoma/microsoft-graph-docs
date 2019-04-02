
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFormat
var format = new WorkbookRangeFormat
{
	ColumnWidth = 135,
	HorizontalAlignment = "Center",
	VerticalAlignment = "Center",
	RowHeight = 49,
	WrapText = false,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$B$1').Format
	.Request()
	.UpdateAsync(format);

```