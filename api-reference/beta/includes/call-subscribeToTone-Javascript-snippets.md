
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const subscribeToTone = {
  clientContext: "d45324c1-fcb5-430a-902c-f20af696537c"
};

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/subscribeToTone')
		.version('beta')
		.post({String : subscribeToTone});
	console.log(res);
} catch (error) {
	throw error;
}

```