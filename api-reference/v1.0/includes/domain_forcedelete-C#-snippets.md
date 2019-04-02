
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var disableUserAccounts = True;

await graphClient.Domains["{id}"]
	.forceDelete(disableUserAccounts);
	.Request()
	.PostAsync()

```