
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "embed";

await graphClient.Me.Drive.Items["{item-id}"]
	.createLink(type,scope);
	.Request()
	.PostAsync()

```