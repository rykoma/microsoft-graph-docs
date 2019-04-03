
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "value-value";

var name = "name-value";

var values = new List<SettingValue>();
values.Add(new SettingValue(name,value));

var directorySetting = new DirectorySetting
{
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.Settings
	.Request()
	.AddAsync(directorySetting);

```