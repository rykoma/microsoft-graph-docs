
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of AdministrativeUnit
var administrativeUnits = new AdministrativeUnit
{
	DisplayName = "displayName-value",
	Description = "description-value",
	Visibility = "visibility-value",
};

await graphClient.AdministrativeUnits["{id}"]
	.Request()
	.UpdateAsync(administrativeUnits);

```