
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const range = {
"values" : [["Hello", "100"],["1/1/2016", null]],
"formula" : [[null, null], [null, "=B1*2"]],
"numberFormat" : [[null,null], ["m-ddd", null]]
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/worksheets('sheet1')/range(address='A1:B2')')
		.version('beta')
		.update({String : range});
	console.log(res);
} catch (error) {
	throw error;
}

```