
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  name: "name-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/add')
		.post({String : add});
	console.log(res);
} catch (error) {
	throw error;
}

```