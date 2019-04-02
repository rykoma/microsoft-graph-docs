
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/contactFolders/{id}/contacts/delta')
		.version('beta')
		.select('displayName')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```