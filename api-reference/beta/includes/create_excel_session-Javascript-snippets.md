
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const createSession = {
  persistChanges: true
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/createSession')
		.version('beta')
		.post({workbook : createSession});
	console.log(res);
} catch (error) {
	throw error;
}

```