
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Message
var messages = new Message
{
	IsRead = "true",
};

await graphClient.Me.Messages["{id}"]
	.Request()
	.UpdateAsync(messages);

```