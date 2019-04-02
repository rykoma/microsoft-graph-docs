
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const move = {
  destinationId: "destinationId-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders/{id}/move')
		.version('beta')
		.post({String : move});
	console.log(res);
} catch (error) {
	throw error;
}

```