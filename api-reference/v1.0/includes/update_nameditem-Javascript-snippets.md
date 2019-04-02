
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const names = {
  type: "type-value",
  scope: "scope-value",
  comment: "comment-value",
  value: {
  },
  visible: true
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/names/{name}')
		.update({workbookNamedItem : names});
	console.log(res);
} catch (error) {
	throw error;
}

```