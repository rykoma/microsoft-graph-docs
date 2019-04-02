
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var participants = new List<String>();

var clientContext = "clientContext-value";

await graphClient.App.Calls["{id}"].Participants
	.muteAll(participants,clientContext);
	.Request()
	.PostAsync()

```