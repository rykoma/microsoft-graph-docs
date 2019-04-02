
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var across = True;

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.range();
	.merge(across);
	.Request()
	.PostAsync()

```