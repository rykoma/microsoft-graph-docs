
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "True";

var name = "EnableGroupCreation";

var valueVar = "";

var nameVar = "ClassificationList";

var valueVarVar = "";

var nameVarVar = "UsageGuidelinesUrl";

var valueVarVarVar = "True";

var nameVarVarVar = "AllowToAddGuests";

var valueVarVarVarVar = "62e90394-69f5-4237-9190-012177145e10";

var nameVarVarVarVar = "GroupCreationAllowedGroupId";

var valueVarVarVarVarVar = "";

var nameVarVarVarVarVar = "GuestUsageGuidelinesUrl";

var valueVarVarVarVarVarVar = "True";

var nameVarVarVarVarVarVar = "AllowGuestsToAccessGroups";

var valueVarVarVarVarVarVarVar = "False";

var nameVarVarVarVarVarVarVar = "AllowGuestsToBeGroupOwner";

var valueVarVarVarVarVarVarVarVar = "";

var nameVarVarVarVarVarVarVarVar = "PrefixSuffixNamingRequirement";

var valueVarVarVarVarVarVarVarVarVar = "";

var nameVarVarVarVarVarVarVarVarVar = "DefaultClassification";

var valueVarVarVarVarVarVarVarVarVarVar = "";

var nameVarVarVarVarVarVarVarVarVarVar = "ClassificationDescriptions";

var valueVarVarVarVarVarVarVarVarVarVarVar = "False";

var nameVarVarVarVarVarVarVarVarVarVarVar = "EnableMSStandardBlockedWords";

var valueVarVarVarVarVarVarVarVarVarVarVarVar = "";

var nameVarVarVarVarVarVarVarVarVarVarVarVar = "CustomBlockedWordsList";

//create SettingValue list and populate it
var valueVarVarVarVarVarVarVarVarVarVarVarVars = new List<SettingValue>();
valueVarVarVarVarVarVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVarVarVarVarVarVar));
valueVarVarVarVarVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVarVarVarVarVar));
valueVarVarVarVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVarVarVarVar));
valueVarVarVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVarVarVar));
valueVarVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVarVar));
valueVarVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVarVar,valueVarVarVarVarVarVarVar));
valueVarVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVarVar,valueVarVarVarVarVarVar));
valueVarVarVarVarVars.Add(new SettingValue(nameVarVarVarVarVar,valueVarVarVarVarVar));
valueVarVarVarVars.Add(new SettingValue(nameVarVarVarVar,valueVarVarVarVar));
valueVarVarVars.Add(new SettingValue(nameVarVarVar,valueVarVarVar));
valueVarVars.Add(new SettingValue(nameVarVar,valueVarVar));
valueVars.Add(new SettingValue(nameVar,valueVar));
values.Add(new SettingValue(name,value));

//create instance of GroupSetting
var groupSettings = new GroupSetting
{
	DisplayName = "displayName-value",
	TemplateId = "templateId-value",
	Values = values,
};

await graphClient.GroupSettings["{id}"]
	.Request()
	.UpdateAsync(groupSettings);

```