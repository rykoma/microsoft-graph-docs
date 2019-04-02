
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeFont
var font = new WorkbookRangeFont
{
	Underline = "Single",
	Color = "#FFFFFF",
	Size = 26,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["Sheet1"].Range('$C$1').Format.Font
	.Request()
	.UpdateAsync(font);

```