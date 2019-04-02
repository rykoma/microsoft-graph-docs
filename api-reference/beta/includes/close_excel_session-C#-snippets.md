
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Items["{id}"].Workbook
	.closeSession(this);
	.Request()
	.PostAsync()

```