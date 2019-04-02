
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const cancel = {
  Comment: "Cancelling for this week due to all hands"
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/cancel')
		.version('beta')
		.post({String : cancel});
	console.log(res);
} catch (error) {
	throw error;
}

```