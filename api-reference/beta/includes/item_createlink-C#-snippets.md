
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "view";

var scope = "anonymous";

await graphClient.Me.Drive.Items["{itemId}"]
	.createLink(type,scope,expirationDateTime,password,message,recipients);
	.Request()
	.PostAsync()

```