
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var groupTypes = new List<String>();

//create instance of Group
var groups = new Group
{
	Description = "description-value",
	DisplayName = "displayName-value",
	GroupTypes = groupTypes,
	Mail = "mail-value",
	MailEnabled = true,
	MailNickname = "mailNickname-value",
};

await graphClient.Groups["{id}"]
	.Request()
	.UpdateAsync(groups);

```