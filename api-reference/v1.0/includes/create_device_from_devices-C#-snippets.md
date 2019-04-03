
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var key = "base64Y3YxN2E1MWFlYw==";

var type = 2;

var alternativeSecurityIds = new List<AlternativeSecurityId>();
alternativeSecurityIds.Add(new AlternativeSecurityId(type,key));

var device = new Device
{
	AccountEnabled = false,
	AlternativeSecurityIds = alternativeSecurityIds,
	DeviceId = "4c299165-6e8f-4b45-a5ba-c5d250a707ff",
	DisplayName = "Test device",
	OperatingSystem = "linux",
	OperatingSystemVersion = "1",
};

await graphClient.Devices
	.Request()
	.AddAsync(device);

```