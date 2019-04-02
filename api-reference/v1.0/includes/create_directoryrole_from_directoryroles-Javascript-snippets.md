
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const directoryRoles = {
  roleTemplateId: "roleTemplateId-value"
};

//make the request to Graph
try{
	let res = await client.api('/directoryRoles')
		.post({directoryRole : directoryRoles});
	console.log(res);
} catch (error) {
	throw error;
}

```