
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tlpLevel = "green";

var threatType = "WatchList";

var targetProduct = "Azure Sentinel";

var tags = new List<String>();

var severity = 0;

var malwareFamilyNames = new List<String>();

var killChain = new List<String>();

var fileHashValue = "1796b433950990b28d6a22456c9d2b58ced1bdfcdf5f16f7e39d6b9bdca4213b";

var fileHashType = "sha256";

var externalId = "Test--8586509942423126760MS164-1";

var expirationDateTime = 3/2/2019 12:44:03 AM;

var description = "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.";

var confidence = 0;

var activityGroupNames = new List<String>();

var tlpLevelVar = "green";

var threatTypeVar = "WatchList";

var targetProductVar = "Azure Sentinel";

var tagsVar = new List<String>();

var severityVar = 0;

var malwareFamilyNamesVar = new List<String>();

var killChainVar = new List<String>();

var fileHashValueVar = "b555c45c5b1b01304217e72118d6ca1b14b7013644a078273cea27bbdc1cf9d6";

var fileHashTypeVar = "sha256";

var externalIdVar = "Test--8586509942423126760MS164-0";

var expirationDateTimeVar = 3/2/2019 12:44:03 AM;

var descriptionVar = "This is a canary indicator for demo purpose. Take no action on any observables set in this indicator.";

var confidenceVar = 0;

var activityGroupNamesVar = new List<String>();

var value = new List<TiIndicator>();
value.Add(new TiIndicator(activityGroupNamesVar,confidenceVar,descriptionVar,expirationDateTimeVar,externalIdVar,fileHashTypeVar,fileHashValueVar,killChainVar,malwareFamilyNamesVar,severityVar,tagsVar,targetProductVar,threatTypeVar,tlpLevelVar));
value.Add(new TiIndicator(activityGroupNames,confidence,description,expirationDateTime,externalId,fileHashType,fileHashValue,killChain,malwareFamilyNames,severity,tags,targetProduct,threatType,tlpLevel));

await graphClient.Security.TiIndicators
	.SubmitTiIndicators(value)
	.Request()
	.PostAsync()

```