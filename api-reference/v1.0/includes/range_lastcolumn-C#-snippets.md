
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var lastColumn = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"].Range().LastColumn()
	.Request()
	.GetAsync();

```