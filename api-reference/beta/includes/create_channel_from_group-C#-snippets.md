
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Channel
var channels = new Channel
{
	DisplayName = "Architecture Discussion",
	Description = "This channel is where we debate all future architecture plans",
};

await graphClient.Teams["{id}"].Channels
	.Request()
	.AddAsync(channels);

```