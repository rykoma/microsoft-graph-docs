
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var inputIds = new List<String>();

var sourceIdType = "restId";

var targetIdType = "restImmutableEntryId";

await graphClient.Me
	.TranslateExchangeIds(inputIds,targetIdType,sourceIdType)
	.Request()
	.PostAsync()

```