
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var icon = new WorkbookIcon
{
	Set = "set-value",
	Index = 99,
};

var dataOption = "dataOption-value";

var color = "color-value";

var ascending = True;

var sortOn = "sortOn-value";

var key = 99;

var fields = new List<WorkbookSortField>();
fields.Add(new WorkbookSortField(key,sortOn,ascending,color,dataOption,icon));

var matchCase = True;

var method = "method-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Sort
	.Apply(fields,matchCase,method)
	.Request()
	.PostAsync()

```