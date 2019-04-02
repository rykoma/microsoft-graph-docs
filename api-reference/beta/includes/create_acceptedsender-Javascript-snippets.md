
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const acceptedSenders = {
  @odata.id:"https://graph.microsoft.com/beta/users/alexd@contoso.com"
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/acceptedSenders/$ref')
		.version('beta')
		.post({directoryObject : acceptedSenders});
	console.log(res);
} catch (error) {
	throw error;
}

```