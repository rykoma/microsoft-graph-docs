
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeBorder = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["name"].Range().Format.Borders
	.Request()
	.GetAsync();

```