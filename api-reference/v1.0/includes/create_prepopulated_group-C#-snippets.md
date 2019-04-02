
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create Bind list and populate it
var members@odata.bind = new List<Bind>();

//create Bind list and populate it
var owners@odata.bind = new List<Bind>();

//create String list and populate it
var groupTypes = new List<String>();

//create instance of Group
var groups = new Group
{
	Description = "Group with designated owner and members",
	DisplayName = "Operations group",
	GroupTypes = groupTypes,
	MailEnabled = true,
	MailNickname = "operations2019",
	SecurityEnabled = false,
	Owners@odata.bind = owners@odata.bind,
	Members@odata.bind = members@odata.bind,
};

await graphClient.Groups
	.Request()
	.AddAsync(groups);

```