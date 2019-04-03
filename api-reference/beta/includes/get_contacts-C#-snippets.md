
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contact = await graphClient.Me.Contacts
	.Request()
	.Select("displayName,emailAddresses")
	.GetAsync();

```