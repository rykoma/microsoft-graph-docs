
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var roles = new List<String>();

//create instance of Permission
var permissions = new Permission
{
	Roles = roles,
};

await graphClient.Me.Drive.Items["{item-id}"].Permissions["{perm-id}"]
	.Request()
	.UpdateAsync(permissions);

```