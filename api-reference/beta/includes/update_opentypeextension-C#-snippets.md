
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create TopPicks list and populate it
var topPicks = new List<TopPicks>();

//create instance of Extension
var extensions = new Extension
{
	@odata.type = "Microsoft.OutlookServices.OpenTypeExtension",
	ExtensionName = "Com.Contoso.Estimate",
	CompanyName = "Contoso",
	ExpirationDate = "2016-07-30T11:00:00Z",
	DealValue = 1010100,
	TopPicks = topPicks,
};

await graphClient.Groups["37df2ff0-0de0-4c33-8aee-75289364aef6"].Threads["AAQkADJizZJpEWwqDHsEpV_KA=="].Posts["AAMkADJiUg96QZUkA-ICwMubAADDEd7UAAA="].Extensions["Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate"]
	.Request()
	.UpdateAsync(extensions);

```