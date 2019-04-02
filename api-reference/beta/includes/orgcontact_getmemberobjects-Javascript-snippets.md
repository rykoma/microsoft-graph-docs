
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMemberObjects = {
  securityEnabledOnly: true
};

//make the request to Graph
try{
	let res = await client.api('/contacts/{id}/getMemberObjects')
		.version('beta')
		.post({Boolean : getMemberObjects});
	console.log(res);
} catch (error) {
	throw error;
}

```