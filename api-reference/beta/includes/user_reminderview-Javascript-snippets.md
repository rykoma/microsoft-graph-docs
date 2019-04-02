
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/reminderView(startDateTime='2017-06-05T10:00:00.0000000',endDateTime='2017-06-11T11:00:00.0000000')')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```