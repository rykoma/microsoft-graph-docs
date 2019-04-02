
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const directoryRoles = {
  description: "description-value",
  displayName: "displayName-value",
  roleTemplateId: "roleTemplateId-value"
};

//make the request to Graph
try{
	let res = await client.api('/directoryRoles')
		.version('beta')
		.post({directoryRole : directoryRoles});
	console.log(res);
} catch (error) {
	throw error;
}

```