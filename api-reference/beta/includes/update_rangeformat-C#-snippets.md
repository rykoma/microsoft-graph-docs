
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFormat
var format = new WorkbookRangeFormat
{
	ColumnWidth = 135,
	VerticalAlignment = "Top",
	RowHeight = 49,
	WrapText = false,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$A$1').Format
	.Request()
	.UpdateAsync(format);

```