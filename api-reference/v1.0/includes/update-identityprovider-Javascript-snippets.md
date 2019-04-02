
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const identityProviders = {
    clientSecret: "1111111111111"
};

//make the request to Graph
try{
	let res = await client.api('/identityProviders/Amazon-OAuth')
		.update({identityProvider : identityProviders});
	console.log(res);
} catch (error) {
	throw error;
}

```