
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var ids = new List<String>();

//create String list and populate it
var types = new List<String>();

await graphClient.DirectoryObjects
	.getByIds(ids,types);
	.Request()
	.PostAsync()

```