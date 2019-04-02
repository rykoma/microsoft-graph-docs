
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const roleSettings = {
  adminEligibleSettings:[{ruleIdentifier:ExpirationRule","setting:{\"permanentAssignment\:false,\maximumGrantPeriodInMinutes\:129600}"}]
};

//make the request to Graph
try{
	let res = await client.api('/privilegedAccess/pimforazurerbac/roleSettings/5fb5aef8-1081-4b8e-bb16-9d5d0385bab5')
		.version('beta')
		.update({governanceRoleSetting : roleSettings});
	console.log(res);
} catch (error) {
	throw error;
}

```