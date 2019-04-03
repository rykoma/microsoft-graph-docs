
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var key = "key-value";

var identityProvider = "identityProvider-value";

var type = 99;

var alternativeSecurityIds = new List<AlternativeSecurityId>();
alternativeSecurityIds.Add(new AlternativeSecurityId(type,identityProvider,key));

var device = new Device
{
	AccountEnabled = true,
	AlternativeSecurityIds = alternativeSecurityIds,
	ApproximateLastSignInDateTime = "2016-10-19T10:37:00Z",
	DeviceId = "deviceId-value",
	DeviceMetadata = "deviceMetadata-value",
	DeviceVersion = 99,
};

await graphClient.Devices
	.Request()
	.AddAsync(device);

```