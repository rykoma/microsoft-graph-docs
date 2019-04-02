
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of MessageRuleActions
var actions = new MessageRuleActions
{
	MarkImportance = "high",
};

//create instance of MessageRule
var messageRules = new MessageRule
{
	DisplayName = "Important from partner",
	Actions = actions,
};

await graphClient.Me.MailFolders["inbox"].MessageRules["AQAAAJ5dZqA="]
	.Request()
	.UpdateAsync(messageRules);

```