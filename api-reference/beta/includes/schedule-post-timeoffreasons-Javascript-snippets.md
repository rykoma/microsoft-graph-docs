
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const timeOffReasons = {
  displayName: "Vacation",
  iconType: "plane",
  isActive: true
}
;

//make the request to Graph
try{
	let res = await client.api('/teams/{teamId}/schedule/timeOffReasons')
		.version('beta')
		.post({timeOffReason : timeOffReasons});
	console.log(res);
} catch (error) {
	throw error;
}

```