
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const groupSettings = {
  displayName: "displayName-value",
  templateId: "templateId-value",
  values: [
    {
      name: "CustomBlockedWordsList",
      value: ""
    },
    {
      name: "EnableMSStandardBlockedWords",
      value: "False"
    },
    {
      name: "ClassificationDescriptions",
      value: ""
    },
    {
      name: "DefaultClassification",
      value: ""
    },
    {
      name: "PrefixSuffixNamingRequirement",
      value: ""
    },
    {
      name: "AllowGuestsToBeGroupOwner",
      value: "False"
    },
    {
      name: "AllowGuestsToAccessGroups",
      value: "True"
    },
    {
      name: "GuestUsageGuidelinesUrl",
      value: ""
    },
    {
      name: "GroupCreationAllowedGroupId",
      value: "62e90394-69f5-4237-9190-012177145e10"
    },
    {
      name: "AllowToAddGuests",
      value: "True"
    },
    {
      name: "UsageGuidelinesUrl",
      value: ""
    },
    {
      name: "ClassificationList",
      value: ""
    },
    {
      name: "EnableGroupCreation",
      value: "True"
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/groupSettings/{id}')
		.update({groupSetting : groupSettings});
	console.log(res);
} catch (error) {
	throw error;
}

```