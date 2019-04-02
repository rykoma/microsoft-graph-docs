
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.range();.Format
	.autofitRows();
	.Request()
	.PostAsync()

```