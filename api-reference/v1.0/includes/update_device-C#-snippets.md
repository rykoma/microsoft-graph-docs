
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Device
var devices = new Device
{
	AccountEnabled = false,
};

await graphClient.Devices["{id}"]
	.Request()
	.UpdateAsync(devices);

```