
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/messages')
		.version('beta')
		.filter('id eq 'Com.Contoso.Referral')')
		.expand('extensions')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```