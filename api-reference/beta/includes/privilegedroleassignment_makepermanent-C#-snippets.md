
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var reason = "reason-value";

var ticketNumber = "ticketNumber-value";

var ticketSystem = "ticketSystem-value";

await graphClient.PrivilegedRoleAssignments["{id}"]
	.makePermanent(reason,ticketNumber,ticketSystem);
	.Request()
	.PostAsync()

```