
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var automaticRepliesSetting = await graphClient.Me.MailboxSettings.AutomaticRepliesSetting
	.Request()
	.GetAsync();

```