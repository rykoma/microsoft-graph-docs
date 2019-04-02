
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
		.header('Prefer','outlook.body-content-type="text"')
		.select('subject,body,bodyPreview,uniqueBody')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```