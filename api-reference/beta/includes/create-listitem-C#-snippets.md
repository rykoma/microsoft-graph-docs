
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of FieldValueSet
var fields = new FieldValueSet
{
	Color = "Fuchsia",
	Quantity = 934,
};

await graphClient.Sites["{site-id}"].Lists["{list-id}"].Items["{item-id}"].Fields
	.Request()
	.UpdateAsync(fields);

```