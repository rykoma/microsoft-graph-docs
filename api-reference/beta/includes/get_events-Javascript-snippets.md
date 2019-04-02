
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/events')
		.version('beta')
		.header('Prefer','outlook.timezone="Pacific Standard Time"')
		.select('subject,body,bodyPreview,organizer,attendees,start,end,location')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```