
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var disableUserAccounts = True;

await graphClient.Domains["contoso.com"]
	.forceDelete(disableUserAccounts);
	.Request()
	.PostAsync()

```