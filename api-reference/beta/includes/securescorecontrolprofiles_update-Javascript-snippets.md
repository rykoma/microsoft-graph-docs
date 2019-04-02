
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const secureScoreControlProfiles = {
  assignedTo: "assignedTo-value",
  controlStateUpdates: "controlStateUpdates-value",
  tenantNote: "tenantNote-value"
};

//make the request to Graph
try{
	let res = await client.api('/security/secureScoreControlProfiles/AdminMFA')
		.version('beta')
		.update({secureScoreControlProfile : secureScoreControlProfiles});
	console.log(res);
} catch (error) {
	throw error;
}

```