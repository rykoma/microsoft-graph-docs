
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const makePermanent = {
  reason: "reason-value",
  ticketNumber: "ticketNumber-value",
  ticketSystem: "ticketSystem-value"
};

//make the request to Graph
try{
	let res = await client.api('/privilegedRoleAssignments/{id}/makePermanent')
		.version('beta')
		.post({String : makePermanent});
	console.log(res);
} catch (error) {
	throw error;
}

```