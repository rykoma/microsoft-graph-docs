
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants["{id}"]
	.mute(clientContext);
	.Request()
	.PostAsync()

```