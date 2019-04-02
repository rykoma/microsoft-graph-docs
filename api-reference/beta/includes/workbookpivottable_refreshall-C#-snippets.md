
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drive.Root.Workbook.Worksheets["{id}"].PivotTables
	.refreshAll();
	.Request()
	.PostAsync()

```