
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EducationSchool
var schools = new EducationSchool
{
	DisplayName = "Fabrikam Arts High School",
	Description = "Magnate school for the arts. Los Angeles School District",
};

await graphClient.Education.Schools["{school-id}"]
	.Request()
	.UpdateAsync(schools);

```