
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var shift = "shift-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["name"]
	.Range()
	.Insert(shift)
	.Request()
	.PostAsync()

```