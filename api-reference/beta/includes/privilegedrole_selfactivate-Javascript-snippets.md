
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const selfActivate = {
  reason: "reason-value",
  duration: "duration-value",
  ticketNumber: "ticketNumber-value",
  ticketSystem: "ticketSystem-value"
};

//make the request to Graph
try{
	let res = await client.api('/privilegedRoles/{id}/selfActivate')
		.version('beta')
		.post({String : selfActivate});
	console.log(res);
} catch (error) {
	throw error;
}

```