
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  index: null,
  values: [
    [1, 2, 3],
    [4, 5, 6]
  ]
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/add')
		.version('beta')
		.post({Int32 : add});
	console.log(res);
} catch (error) {
	throw error;
}

```