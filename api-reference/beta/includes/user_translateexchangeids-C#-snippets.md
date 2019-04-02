
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var inputIds = new List<String>();

var sourceIdType = "restId";

var targetIdType = "restImmutableEntryId";

await graphClient.Me
	.TranslateExchangeIds(inputIds,targetIdType,sourceIdType)
	.Request()
	.PostAsync()

```