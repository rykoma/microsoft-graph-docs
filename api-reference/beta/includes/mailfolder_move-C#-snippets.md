
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var destinationId = "destinationId-value";

await graphClient.Me.MailFolders["{id}"]
	.move(destinationId);
	.Request()
	.PostAsync()

```