
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFormat
var format = new WorkbookRangeFormat
{
	ColumnWidth = 135,
	HorizontalAlignment = "Right",
	VerticalAlignment = "Top",
	RowHeight = 49,
	WrapText = false,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{sheet-id}"].Range('$C$1').Format
	.Request()
	.UpdateAsync(format);

```