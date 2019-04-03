
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var EmailAddresses = new List<String>();

var MailTipsOptions = "automaticReplies, mailboxFullStatus";

await graphClient.Me
	.GetMailTips(emailAddresses,mailTipsOptions)
	.Request()
	.PostAsync()

```