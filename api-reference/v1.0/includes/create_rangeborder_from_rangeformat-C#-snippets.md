
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookRangeBorder
var borders = new WorkbookRangeBorder
{
	Id = "id-value",
	Color = "color-value",
	Style = "style-value",
	SideIndex = "sideIndex-value",
	Weight = "weight-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.Range().Format.Borders
	.Request()
	.AddAsync(borders);

```