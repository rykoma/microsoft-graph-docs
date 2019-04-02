
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/events/AAMkADAGAADDdm4NAAA=')
		.select('subject,body,bodyPreview,organizer,attendees,start,end,location,locations')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```