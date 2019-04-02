
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const add = {
  address: "Sheet1!A1:D5",
  hasHeaders: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/add')
		.post({String : add});
	console.log(res);
} catch (error) {
	throw error;
}

```