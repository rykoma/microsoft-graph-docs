
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const updateMetadata = {
  metadata: "metadata-value",
  clientContext: "clientContext-value"
};

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/updateMetadata')
		.version('beta')
		.post({String : updateMetadata});
	console.log(res);
} catch (error) {
	throw error;
}

```