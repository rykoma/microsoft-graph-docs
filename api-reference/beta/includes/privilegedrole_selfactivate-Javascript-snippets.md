
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const selfActivate = {
  reason: "reason-value",
  duration: "duration-value",
  ticketNumber: "ticketNumber-value",
  ticketSystem: "ticketSystem-value"
};

let res = await client.api('/privilegedRoles/{id}/selfActivate')
	.version('beta')
	.post({String : selfActivate});

```