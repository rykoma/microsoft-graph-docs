
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/reports/getOffice365ActiveUserCounts(period='D7')')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```