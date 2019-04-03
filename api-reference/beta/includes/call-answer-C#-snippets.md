
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var callbackUri = "callbackUri-value";

var mediaConfig = new String
{
	@odata.type = "#microsoft.graph.appHostedMediaConfig",
	Blob = "<media config blob>",
};

var acceptedModalities = new List<String>();

await graphClient.App.Calls["{id}"]
	.Answer(callbackUri,mediaConfig,acceptedModalities)
	.Request()
	.PostAsync()

```