
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Drive.Root.Workbook.Worksheets["{id}"]
	.range();
	.rowsBelow(count);
	.Request()
	.PostAsync()

```