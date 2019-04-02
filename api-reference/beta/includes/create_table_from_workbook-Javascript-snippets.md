
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  address: "A1:D8",
  hasHeaders: false
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/$/add')
		.version('beta')
		.post({String : add});
	console.log(res);
} catch (error) {
	throw error;
}

```