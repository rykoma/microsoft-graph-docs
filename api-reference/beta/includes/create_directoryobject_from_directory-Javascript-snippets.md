
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb/restore')
		.version('beta')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```