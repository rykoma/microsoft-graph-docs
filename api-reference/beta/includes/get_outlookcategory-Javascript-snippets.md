
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/outlook/masterCategories('de912e4d-c790-4da9-949c-ccd933aaa0f7')')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```