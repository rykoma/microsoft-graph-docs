
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const addFormulaLocal = {
  name: "test7",
  formula: "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  comment: "Comment for the named item"
};

let res = await client.api('/me/drive/items/{id}/workbook/names/addFormulaLocal')
	.post({String : addFormulaLocal});

```