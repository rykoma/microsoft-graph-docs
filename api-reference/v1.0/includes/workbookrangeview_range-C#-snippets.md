
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var range = await graphClient.Me.Drive.Root.Workbook.Worksheets["{id}"].Range('A1:Z10').VisibleView().Range()
	.Request()
	.GetAsync();

```