
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EducationClass
var classes = new EducationClass
{
	Description = "History - World History 1",
	DisplayName = "World History Level 1",
};

await graphClient.Education.Classes["{class-id}"]
	.Request()
	.UpdateAsync(classes);

```