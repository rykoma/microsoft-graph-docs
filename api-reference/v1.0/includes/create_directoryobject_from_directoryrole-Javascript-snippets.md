
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const members = {
  @odata.id: "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
};

//make the request to Graph
try{
	let res = await client.api('/directoryRoles/{id}/members/$ref')
		.post({directoryObject : members});
	console.log(res);
} catch (error) {
	throw error;
}

```