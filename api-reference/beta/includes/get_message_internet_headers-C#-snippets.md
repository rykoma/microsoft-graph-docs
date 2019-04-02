
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var messages = await graphClient.Me.Messages["AAMkAGVmMDEz"]
	.Request()
	.Select("internetMessageHeaders")
	.GetAsync();

```