
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"]
	.range();
	.rowsBelow(count);
	.Request()
	.PostAsync()

```