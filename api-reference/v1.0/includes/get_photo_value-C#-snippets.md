
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var $value = await graphClient.Users["{id|userPrincipalName}"].Photo.$value
	.Request()
	.GetAsync();

```