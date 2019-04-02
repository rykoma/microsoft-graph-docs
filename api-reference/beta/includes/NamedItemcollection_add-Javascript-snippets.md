
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const addFormulaLocal = {
  name: "test7",
  formula: "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  comment: "Comment for the named item"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/addFormulaLocal')
		.version('beta')
		.post({String : addFormulaLocal});
	console.log(res);
} catch (error) {
	throw error;
}

```