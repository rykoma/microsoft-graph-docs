
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );


var values = new List<Int32>();

await graphClient.Me.Drive.Items["{id}"].Workbook.Tables["{id|name}"].Rows
	.Add(index,values)
	.Request()
	.PostAsync()

```