
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const deleteTiIndicatorsByExternalId = {
  value: [
    "externalId-value1",
    "externalId-value2"
  ]
};

//make the request to Graph
try{
	let res = await client.api('/security/tiIndicators/deleteTiIndicatorsByExternalId')
		.version('beta')
		.post({String : deleteTiIndicatorsByExternalId});
	console.log(res);
} catch (error) {
	throw error;
}

```