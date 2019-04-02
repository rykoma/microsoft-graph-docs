
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var supportedServices = new List<String>();

//create instance of Domain
var domains = new Domain
{
	IsDefault = true,
	SupportedServices = supportedServices,
};

await graphClient.Domains["contoso.com"]
	.Request()
	.UpdateAsync(domains);

```