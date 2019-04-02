
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Application
var applications = new Application
{
	AllowPublicClient = false,
	DisplayName = "New display name",
};

await graphClient.Applications["{id}"]
	.Request()
	.UpdateAsync(applications);

```