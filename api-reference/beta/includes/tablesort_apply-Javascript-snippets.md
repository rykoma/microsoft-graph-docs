
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const apply = {
  fields: [
    {
      key: 99,
      sortOn: "sortOn-value",
      ascending: true,
      color: "color-value",
      dataOption: "dataOption-value",
      icon: {
        set: "set-value",
        index: 99
      }
    }
  ],
  matchCase: true,
  method: "method-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply')
		.version('beta')
		.post({workbookSortField : apply});
	console.log(res);
} catch (error) {
	throw error;
}

```