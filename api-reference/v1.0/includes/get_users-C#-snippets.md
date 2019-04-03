
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var user = await graphClient.Users
	.Request()
	.Select("displayName,givenName,postalCode")
	.GetAsync();

```