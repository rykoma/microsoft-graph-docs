
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "value-value";

var name = "name-value";

//create SettingValue list and populate it
var values = new List<SettingValue>();
values.Add(new SettingValue(name,value));

//create instance of DirectorySetting
var settings = new DirectorySetting
{
	Values = values,
};

await graphClient.Settings["{id}"]
	.Request()
	.UpdateAsync(settings);

```