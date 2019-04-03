
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var outlookCategory = new OutlookCategory
{
	DisplayName = "Project expenses",
	Color = "preset9",
};

await graphClient.Me.Outlook.MasterCategories
	.Request()
	.AddAsync(outlookCategory);

```