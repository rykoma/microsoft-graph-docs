
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var EntireColumn = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["name"].Range().EntireColumn()
	.Request()
	.GetAsync();

```