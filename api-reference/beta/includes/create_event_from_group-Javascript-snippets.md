
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const events = {
  originalStartTimeZone: "originalStartTimeZone-value",
  originalEndTimeZone: "originalEndTimeZone-value",
  responseStatus: {
    response: "",
    time: "2016-10-19T10:37:00Z"
  },
  uid: "iCalUId-value",
  reminderMinutesBeforeStart: 99,
  isReminderOn: true
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/events')
		.version('beta')
		.post({event : events});
	console.log(res);
} catch (error) {
	throw error;
}

```