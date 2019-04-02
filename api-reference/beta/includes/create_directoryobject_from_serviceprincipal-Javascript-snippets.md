
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const owners = {
  directoryObject: {
  }
};

//make the request to Graph
try{
	let res = await client.api('/servicePrincipals/{id}/owners')
		.version('beta')
		.post({directoryObject : owners});
	console.log(res);
} catch (error) {
	throw error;
}

```