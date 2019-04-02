
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "edit";

var scope = "organization";

await graphClient.Me.Drive.Items["{item-id}"]
	.createLink(type,scope);
	.Request()
	.PostAsync()

```