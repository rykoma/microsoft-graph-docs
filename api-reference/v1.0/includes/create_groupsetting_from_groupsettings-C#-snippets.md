
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "value-value";

var name = "name-value";

var values = new List<SettingValue>();
values.Add(new SettingValue(name,value));

var groupSetting = new GroupSetting
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.GroupSettings
	.Request()
	.AddAsync(groupSetting);

```