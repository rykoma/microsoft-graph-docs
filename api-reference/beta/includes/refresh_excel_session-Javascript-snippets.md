
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const refreshSession = {

}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{id}/workbook/refreshSession')
		.version('beta')
		.post({workbook : refreshSession});
	console.log(res);
} catch (error) {
	throw error;
}

```