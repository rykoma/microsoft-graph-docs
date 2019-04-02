
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/events/AAMkAGUzYRgWAAA=/instances')
		.version('beta')
		.select('subject,bodyPreview,seriesMasterId,type,recurrence,start,end')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```