
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var index = new Int32
{
};

var values = new List<Int32>();
values.Add(new Int32());

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Columns
	.Add(index,values,name)
	.Request()
	.PostAsync()

```