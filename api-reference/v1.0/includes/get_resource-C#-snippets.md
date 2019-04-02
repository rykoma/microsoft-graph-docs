
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var content = await graphClient.Me.Onenote.Resources["{id}"].Content
	.Request()
	.GetAsync();

```