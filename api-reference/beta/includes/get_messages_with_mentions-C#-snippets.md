
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages
	.Request()
	.Filter("MentionsPreview/IsMentioned eq true,")
	.Select("subject,sender,receivedDateTime,mentionsPreview")
	.GetAsync();

```