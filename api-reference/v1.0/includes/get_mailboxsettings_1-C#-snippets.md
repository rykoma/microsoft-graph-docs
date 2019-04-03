
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailboxSettings = await graphClient.Me.MailboxSettings
	.Request()
	.GetAsync();

```