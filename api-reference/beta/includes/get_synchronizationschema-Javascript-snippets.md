
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/servicePrincipals/{servicePrincipalId}/synchronization/jobs/{jobId}/schema')
		.version('beta')
		.header('Authorization','Bearer {Token}')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```