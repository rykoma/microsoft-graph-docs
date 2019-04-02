
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calendars = {
  name: "Volunteer"
}

;

//make the request to Graph
try{
	let res = await client.api('/me/calendars')
		.version('beta')
		.post({calendar : calendars});
	console.log(res);
} catch (error) {
	throw error;
}

```