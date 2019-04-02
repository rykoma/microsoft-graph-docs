
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of SecureScoreControlProfile
var secureScoreControlProfiles = new SecureScoreControlProfile
{
	AssignedTo = "assignedTo-value",
	ControlStateUpdates = "controlStateUpdates-value",
	TenantNote = "tenantNote-value",
};

await graphClient.Security.SecureScoreControlProfiles["AdminMFA"]
	.Request()
	.UpdateAsync(secureScoreControlProfiles);

```