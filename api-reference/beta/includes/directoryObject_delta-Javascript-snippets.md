
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/directoryObjects/delta')
		.version('beta')
		.filter('isOf('Microsoft.Graph.User')+or+isOf('Microsoft.Graph.Group')')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```