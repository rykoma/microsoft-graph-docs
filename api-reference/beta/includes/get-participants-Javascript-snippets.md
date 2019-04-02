
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/app/calls/57DAB8B1894C409AB240BD8BEAE78896/participants')
		.version('beta')
		.header('Authorization','Bearer <TOKEN>')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```