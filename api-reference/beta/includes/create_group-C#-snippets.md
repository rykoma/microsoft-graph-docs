
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupTypes = new List<String>();

var group = new Group
{
	Description = "Self help community for golf",
	DisplayName = "Golf Assist",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "golfassist",
	SecurityEnabled = false,
};

await graphClient.Groups
	.Request()
	.AddAsync(group);

```