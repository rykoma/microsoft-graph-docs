
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const clear = {
  applyTo: "applyTo-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names('name')/range/clear')
		.version('beta')
		.post({String : clear});
	console.log(res);
} catch (error) {
	throw error;
}

```