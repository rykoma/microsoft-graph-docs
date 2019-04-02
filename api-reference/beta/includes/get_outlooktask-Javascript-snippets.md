
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/outlook/tasks('AAMkADA1MHgwAAA=')')
		.version('beta')
		.header('Prefer','outlook.timezone="Pacific Standard Time"')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```