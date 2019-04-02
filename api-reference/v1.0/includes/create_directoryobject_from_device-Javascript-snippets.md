
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const registeredUsers = {
  directoryObject: {
  }
};

//make the request to Graph
try{
	let res = await client.api('/devices/{id}/registeredUsers')
		.post({directoryObject : registeredUsers});
	console.log(res);
} catch (error) {
	throw error;
}

```