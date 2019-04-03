
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var ids = new List<String>();

var types = new List<String>();

await graphClient.DirectoryObjects
	.GetByIds(ids,types)
	.Request()
	.PostAsync()

```