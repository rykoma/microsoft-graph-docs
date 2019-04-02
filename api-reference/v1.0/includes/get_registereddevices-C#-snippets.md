
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var registeredDevices = await graphClient.Me.RegisteredDevices
	.Request()
	.GetAsync();

```