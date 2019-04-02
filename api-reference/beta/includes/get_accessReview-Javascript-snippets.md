
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```