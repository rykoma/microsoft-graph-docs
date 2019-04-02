
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const subscriptions = {
   expirationDateTime:"2016-11-22T18:23:45.9356913Z"
};

//make the request to Graph
try{
	let res = await client.api('/subscriptions/{id}')
		.version('beta')
		.update({subscription : subscriptions});
	console.log(res);
} catch (error) {
	throw error;
}

```