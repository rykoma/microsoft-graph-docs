
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const rejectedSenders = {
  @odata.id:"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/rejectedSenders/$ref')
		.post({directoryObject : rejectedSenders});
	console.log(res);
} catch (error) {
	throw error;
}

```