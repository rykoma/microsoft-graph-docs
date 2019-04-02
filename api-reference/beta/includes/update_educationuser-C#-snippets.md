
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EducationUser
var users = new EducationUser
{
	DisplayName = "Rogelio Cazares",
	GivenName = "Rogelio",
	MiddleName = "Fernando",
	Surname = "Cazares",
};

await graphClient.Education.Users["13020"]
	.Request()
	.UpdateAsync(users);

```