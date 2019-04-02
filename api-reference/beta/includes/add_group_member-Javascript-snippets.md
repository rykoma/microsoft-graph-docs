
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const members = {
  @odata.id: "https://graph.microsoft.com/beta/directoryObjects/{id}"
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/members/$ref')
		.version('beta')
		.post({directoryObject : members});
	console.log(res);
} catch (error) {
	throw error;
}

```