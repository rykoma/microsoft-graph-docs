
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"]
	.range();
	.columnsBefore(count);
	.Request()
	.PostAsync()

```