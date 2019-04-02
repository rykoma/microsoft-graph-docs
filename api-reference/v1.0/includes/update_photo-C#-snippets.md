
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ProfilePhoto
var photo = new ProfilePhoto
{
	Height = 99,
	Width = 99,
	Id = "id-value",
};

await graphClient.Users["{id|userPrincipalName}"].Photo
	.Request()
	.UpdateAsync(photo);

```