
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var destinationId = "deleteditems";

await graphClient.Me.Messages["AAMkADhAAATs28OAAA="]
	.move(destinationId);
	.Request()
	.PostAsync()

```