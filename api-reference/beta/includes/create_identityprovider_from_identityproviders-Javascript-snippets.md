
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const identityProviders = {
    name: "Login with Amazon",
    type: "Amazon",
    clientId: "56433757-cadd-4135-8431-2c9e3fd68ae8",
    clientSecret: "000000000000"
}
;

//make the request to Graph
try{
	let res = await client.api('/identityProviders')
		.version('beta')
		.post({identityProvider : identityProviders});
	console.log(res);
} catch (error) {
	throw error;
}

```