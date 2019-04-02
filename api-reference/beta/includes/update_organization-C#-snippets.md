
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create String list and populate it
var technicalNotificationMails = new List<String>();

//create String list and populate it
var securityComplianceNotificationPhones = new List<String>();

//create String list and populate it
var securityComplianceNotificationMails = new List<String>();

//create instance of PrivacyProfile
var privacyProfile = new PrivacyProfile
{
	ContactEmail = "alice@contoso.com",
	StatementUrl = "https://contoso.com/privacyStatement",
};

//create String list and populate it
var marketingNotificationEmails = new List<String>();

//create instance of Organization
var organization = new Organization
{
	MarketingNotificationEmails = marketingNotificationEmails,
	PrivacyProfile = privacyProfile,
	SecurityComplianceNotificationMails = securityComplianceNotificationMails,
	SecurityComplianceNotificationPhones = securityComplianceNotificationPhones,
	TechnicalNotificationMails = technicalNotificationMails,
};

await graphClient.Organization["{id}"]
	.Request()
	.UpdateAsync(organization);

```