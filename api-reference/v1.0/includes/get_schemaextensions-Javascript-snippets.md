
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/schemaExtensions')
		.filter('id eq 'graphlearn_test'')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```