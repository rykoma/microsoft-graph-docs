
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const owners = {
  @odata.id: "https://graph.microsoft.com/beta/users/{id}"
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/owners/$ref')
		.version('beta')
		.post({directoryObject : owners});
	console.log(res);
} catch (error) {
	throw error;
}

```