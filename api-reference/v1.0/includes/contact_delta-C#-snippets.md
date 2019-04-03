
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contact = await graphClient.Me.ContactFolders["{id}"].Contacts.Delta()
	.Request()
	.Header("Prefer","odata.maxpagesize=2")
	.Select("displayName")
	.GetAsync();

```