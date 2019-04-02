
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/resetDecisions()')
		.version('beta')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```