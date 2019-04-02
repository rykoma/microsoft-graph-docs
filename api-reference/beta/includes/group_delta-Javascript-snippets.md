
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/groups/delta')
		.version('beta')
		.header('Prefer','return=minimal')
		.select('displayName,description,mailNickname')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```