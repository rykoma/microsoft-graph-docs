
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const administrativeUnits = {
  displayName: "displayName-value",
  description: "description-value",
  visibility: "visibility-value"
};

//make the request to Graph
try{
	let res = await client.api('/administrativeUnits/{id}')
		.version('beta')
		.update({administrativeUnit : administrativeUnits});
	console.log(res);
} catch (error) {
	throw error;
}

```