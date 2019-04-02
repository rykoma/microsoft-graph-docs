
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var businessPhones = new List<String>();

//create instance of User
var me = new User
{
	AccountEnabled = true,
	BusinessPhones = businessPhones,
	City = "city-value",
};

await graphClient.Me
	.Request()
	.UpdateAsync(me);

```