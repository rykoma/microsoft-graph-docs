
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const deleteTiIndicators = {
  value: [
    "id-value1",
    "id-value2"
  ]
};

//make the request to Graph
try{
	let res = await client.api('/security/tiIndicators/deleteTiIndicators')
		.version('beta')
		.post({String : deleteTiIndicators});
	console.log(res);
} catch (error) {
	throw error;
}

```