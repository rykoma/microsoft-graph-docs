
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Agreement
var agreements = new Agreement
{
	DisplayName = "displayName-value",
	IsViewingBeforeAcceptanceRequired = true,
};

await graphClient.Agreements["'id'"]
	.Request()
	.UpdateAsync(agreements);

```