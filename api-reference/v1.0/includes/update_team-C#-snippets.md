
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of TeamFunSettings
var funSettings = new TeamFunSettings
{
	AllowGiphy = true,
	GiphyContentRating = "strict",
};

//create instance of TeamMessagingSettings
var messagingSettings = new TeamMessagingSettings
{
	AllowUserEditMessages = true,
	AllowUserDeleteMessages = true,
};

//create instance of TeamMemberSettings
var memberSettings = new TeamMemberSettings
{
	AllowCreateUpdateChannels = true,
};

//create instance of Team
var teams = new Team
{
	MemberSettings = memberSettings,
	MessagingSettings = messagingSettings,
	FunSettings = funSettings,
};

await graphClient.Teams["{id}"]
	.Request()
	.UpdateAsync(teams);

```