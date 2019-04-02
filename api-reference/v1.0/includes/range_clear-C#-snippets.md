
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var applyTo = "applyTo-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
	.range();
	.clear(applyTo);
	.Request()
	.PostAsync()

```