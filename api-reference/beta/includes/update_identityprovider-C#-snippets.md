
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of IdentityProvider
var identityProviders = new IdentityProvider
{
	ClientSecret = "1111111111111",
};

await graphClient.IdentityProviders["Amazon-OAuth"]
	.Request()
	.UpdateAsync(identityProviders);

```