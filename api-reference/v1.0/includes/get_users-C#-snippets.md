
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var users = await graphClient.Users
	.Request()
	.Select("displayName,givenName,postalCode")
	.GetAsync();

```