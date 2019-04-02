
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  index: {
  },
  values: [
    {
    }
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/add')
		.version('beta')
		.post({Int32 : add});
	console.log(res);
} catch (error) {
	throw error;
}

```