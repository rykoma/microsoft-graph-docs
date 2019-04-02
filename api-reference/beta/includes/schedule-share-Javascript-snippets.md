
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const share = {
  notifyTeam: true,
  startDateTime: "2018-10-08T00:00:00.000Z",
  endDateTime: "2018-10-15T00:00:00.000Z"
}
;

//make the request to Graph
try{
	let res = await client.api('/teams/{teamId}/schedule/share')
		.version('beta')
		.post({Boolean : share});
	console.log(res);
} catch (error) {
	throw error;
}

```