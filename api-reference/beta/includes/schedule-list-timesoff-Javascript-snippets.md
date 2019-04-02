
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/teams/{teamId}/schedule/timesOff')
		.version('beta')
		.filter('sharedTimeOff/startDateTime ge 2019-03-11T00:00:00.000Z and sharedTimeOff/endDateTime le 2019-03-18T00:00:00.000Z and draftTimeOff/startDateTime ge 2019-03-11T00:00:00.000Z and draftTimeOff/endDateTime le 2019-03-18T00:00:00.000Z')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```