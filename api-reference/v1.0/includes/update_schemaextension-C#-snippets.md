
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "additional-type-value";

var name = "additional-name-value";

var typeVar = "new-typeVar-value";

var nameVar = "new-nameVar-value";

//create ExtensionSchemaProperty list and populate it
var properties = new List<ExtensionSchemaProperty>();
properties.Add(new ExtensionSchemaProperty(nameVar,typeVar));
properties.Add(new ExtensionSchemaProperty(name,type));

//create instance of SchemaExtension
var schemaExtensions = new SchemaExtension
{
	Properties = properties,
};

await graphClient.SchemaExtensions["{id}"]
	.Request()
	.UpdateAsync(schemaExtensions);

```