
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const merge = {
  across: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/{name}/range/merge')
		.post({Boolean : merge});
	console.log(res);
} catch (error) {
	throw error;
}

```