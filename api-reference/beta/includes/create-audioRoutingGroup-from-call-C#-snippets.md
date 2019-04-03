
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var receivers = new List<String>();

var sources = new List<String>();

var AudioRoutingGroup = new AudioRoutingGroup
{
	Id = "oneToOne",
	RoutingMode = "oneToOne",
	Sources = sources,
	Receivers = receivers,
};

await graphClient.App.Calls["{id}"].AudioRoutingGroups
	.Request()
	.AddAsync(AudioRoutingGroup);

```