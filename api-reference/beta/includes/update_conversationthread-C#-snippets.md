
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ConversationThread
var threads = new ConversationThread
{
	@odata.type = "#Microsoft.OutlookServices.ConversationThread",
	IsLocked = true,
};

await graphClient.Groups["{id}"].Threads["{id}"]
	.Request()
	.UpdateAsync(threads);

```