
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  index: 5,
  values: [
    [1, 2, 3],
    [4, 5, 6]
  ]
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/rows/add')
		.post({Int32 : add});
	console.log(res);
} catch (error) {
	throw error;
}

```