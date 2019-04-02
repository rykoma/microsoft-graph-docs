
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const mute = {
  clientContext: "clientContext-value"
};

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/mute')
		.version('beta')
		.post({String : mute});
	console.log(res);
} catch (error) {
	throw error;
}

```