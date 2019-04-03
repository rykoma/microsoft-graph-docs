
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var vendorInformation = new SecurityVendorInformation
{
	Provider = "Windows Defender ATP",
	Vendor = "Microsoft",
};

var value = "1.2.3.4";

var name = "IP";

var parameters = new List<KeyValuePair>();
parameters.Add(new KeyValuePair(name,value));

var securityAction = new SecurityAction
{
	Name = "BlockIp",
	ActionReason = "Test",
	Parameters = parameters,
	VendorInformation = vendorInformation,
};

await graphClient.Security.SecurityActions
	.Request()
	.AddAsync(securityAction);

```