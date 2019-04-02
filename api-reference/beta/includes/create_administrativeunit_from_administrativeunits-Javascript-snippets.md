
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const administrativeUnits = {
    displayName: "Seattle District Technical Schools",
    description: "Seattle district technical schools administration",
    visibility: "true"
};

//make the request to Graph
try{
	let res = await client.api('/administrativeUnits')
		.version('beta')
		.post({administrativeUnit : administrativeUnits});
	console.log(res);
} catch (error) {
	throw error;
}

```