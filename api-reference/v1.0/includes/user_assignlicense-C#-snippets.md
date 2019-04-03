
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var skuId = "guid";

var disabledPlans = new List<Guid>();

var addLicenses = new List<AssignedLicense>();
addLicenses.Add(new AssignedLicense(disabledPlans,skuId));

var removeLicenses = new List<AssignedLicense>();

await graphClient.Me
	.AssignLicense(addLicenses,removeLicenses)
	.Request()
	.PostAsync()

```