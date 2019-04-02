
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calculate = {
  calculationType: "calculationType-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/application/calculate')
		.version('beta')
		.post({String : calculate});
	console.log(res);
} catch (error) {
	throw error;
}

```