
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var role = "viewer";

await graphClient.App.Calls["{id}"]
	.changeScreenSharingRole(role);
	.Request()
	.PostAsync()

```