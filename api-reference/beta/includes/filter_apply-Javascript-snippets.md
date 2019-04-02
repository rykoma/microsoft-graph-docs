
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const apply = {
  criteria: {
    criterion1: "criterion1-value",
    criterion2: "criterion2-value",
    color: "color-value",
    operator: {
    },
    icon: {
      set: "set-value",
      index: 99
    },
    dynamicCriteria: "dynamicCriteria-value",
    values: {
    },
    filterOn: "filterOn-value"
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/apply')
		.version('beta')
		.post({workbookFilterCriteria : apply});
	console.log(res);
} catch (error) {
	throw error;
}

```