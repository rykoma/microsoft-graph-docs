
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const makePermanent = {
  reason: "reason-value",
  ticketNumber: "ticketNumber-value",
  ticketSystem: "ticketSystem-value"
};

let res = await client.api('/privilegedRoleAssignments/{id}/makePermanent')
	.version('beta')
	.post({String : makePermanent});

```