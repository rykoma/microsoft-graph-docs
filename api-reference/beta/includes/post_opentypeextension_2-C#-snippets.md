
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var extension = new Extension
{
	@odata.type = "Microsoft.Graph.OpenTypeExtension",
	ExtensionName = "Com.Contoso.Referral",
	CompanyName = "Wingtip Toys",
	DealValue = 500050,
	ExpirationDate = "2015-12-03T10:00:00Z",
};

await graphClient.Me.Messages["AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="].Extensions
	.Request()
	.AddAsync(extension);

```