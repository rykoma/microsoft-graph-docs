
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of OutlookCategory
var masterCategories = new OutlookCategory
{
	Color = "preset15",
};

await graphClient.Me.Outlook.MasterCategories["bac262b7-485d-4739-b436-e31467d64fac"]
	.Request()
	.UpdateAsync(masterCategories);

```