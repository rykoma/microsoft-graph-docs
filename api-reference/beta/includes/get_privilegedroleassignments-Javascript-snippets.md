
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/privilegedRoleAssignments')
		.version('beta')
		.filter('isElevated eq true and expirationDateTime ne null or isElevated eq false')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```