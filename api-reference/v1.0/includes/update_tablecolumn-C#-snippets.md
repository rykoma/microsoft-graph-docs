
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of WorkbookTableColumn
var columns = new WorkbookTableColumn
{
	Name = "name-value",
	Index = 99,
	Values = "values-value",
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns["{id|name}"]
	.Request()
	.UpdateAsync(columns);

```