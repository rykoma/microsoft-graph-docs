
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupTypes = new List<String>();

var group = new Group
{
	Description = "Self help community for library",
	DisplayName = "Library Assist",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "library",
	SecurityEnabled = false,
};

await graphClient.Groups
	.Request()
	.AddAsync(group);

```