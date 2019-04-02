
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const channels = {
  displayName: "Architecture Discussion",
  description: "This channel is where we debate all future architecture plans"
};

//make the request to Graph
try{
	let res = await client.api('/teams/{id}/channels')
		.version('beta')
		.post({channel : channels});
	console.log(res);
} catch (error) {
	throw error;
}

```