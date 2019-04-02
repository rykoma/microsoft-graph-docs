
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/programs('673a7379-9c38-4f01-bd9d-4fda7260b807')/controls')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```