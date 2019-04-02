
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var businessPhones = new List<String>();

//create instance of OrgContact
var contacts = new OrgContact
{
	BusinessPhones = businessPhones,
	City = "city-value",
	CompanyName = "companyName-value",
	Country = "country-value",
	Department = "department-value",
	DisplayName = "displayName-value",
};

await graphClient.Contacts["{id}"]
	.Request()
	.UpdateAsync(contacts);

```