
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var privilegedApproval = new PrivilegedApproval
{
	UserId = "userId-value",
	RoleId = "roleId-value",
	ApprovalType = "approvalType-value",
	ApprovalState = "approvalState-value",
	ApprovalDuration = "datetime-value",
};

await graphClient.PrivilegedApproval
	.Request()
	.AddAsync(privilegedApproval);

```