
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
  isRead: "true",
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/{id}')
		.version('beta')
		.update({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```