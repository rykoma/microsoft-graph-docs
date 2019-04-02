
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const unmute = {
  clientContext: "clientContext-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/unmute')
		.version('beta')
		.post({String : unmute});
	console.log(res);
} catch (error) {
	throw error;
}

```