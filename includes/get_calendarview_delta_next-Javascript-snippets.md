
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/calendarView/delta')
		.header('Prefer','odata.maxpagesize=2')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```