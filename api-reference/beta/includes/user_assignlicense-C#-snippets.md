
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var skuId = "skuId-value-2";

var disabledPlans = new List<Guid>();

var skuIdVar = "skuIdVar-value-1";

var disabledPlansVar = new List<Guid>();

var addLicenses = new List<AssignedLicense>();
addLicenses.Add(new AssignedLicense(disabledPlansVar,skuIdVar));
addLicenses.Add(new AssignedLicense(disabledPlans,skuId));

var removeLicenses = new List<AssignedLicense>();

await graphClient.Me
	.AssignLicense(addLicenses,removeLicenses)
	.Request()
	.PostAsync()

```