
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var participants = new List<String>();

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants
	.MuteAll(participants,clientContext)
	.Request()
	.PostAsync()

```