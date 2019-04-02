
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/rows')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```