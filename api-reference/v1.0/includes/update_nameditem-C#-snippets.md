
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Json
var value = new Json
{
};

//create instance of WorkbookNamedItem
var names = new WorkbookNamedItem
{
	Type = "type-value",
	Scope = "scope-value",
	Comment = "comment-value",
	Value = value,
	Visible = true,
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.Request()
	.UpdateAsync(names);

```