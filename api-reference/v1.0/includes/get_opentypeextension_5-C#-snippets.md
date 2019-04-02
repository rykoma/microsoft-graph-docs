
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messages = await graphClient.Me.Messages
	.Request()
	.Filter("id eq 'Com.Contoso.Referral')")
	.Expand("extensions")
	.GetAsync();

```