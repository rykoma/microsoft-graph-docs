
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"].PivotTables
	.refreshAll();
	.Request()
	.PostAsync()

```