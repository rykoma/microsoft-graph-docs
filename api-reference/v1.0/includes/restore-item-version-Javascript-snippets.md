
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/drives/{drive-id}/items/{item-id}/versions/{version-id}/restoreVersion')
		.post();
	console.log(res);
} catch (error) {
	throw error;
}

```