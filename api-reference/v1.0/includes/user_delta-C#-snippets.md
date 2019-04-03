
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var user = await graphClient.Users.Delta()
	.Request()
	.Header("Prefer","return=minimal")
	.Select("displayName,jobTitle,mobilePhone")
	.GetAsync();

```