
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const setPosition = {
  startCell: "startCell-value",
  endCell: "endCell-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setPosition')
		.post({Json : setPosition});
	console.log(res);
} catch (error) {
	throw error;
}

```