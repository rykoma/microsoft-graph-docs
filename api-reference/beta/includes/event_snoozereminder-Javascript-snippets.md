
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const snoozeReminder = {
  newReminderTime: {
    dateTime: "2016-10-19T10:37:00Z",
    timeZone: "timeZone-value"
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/snoozeReminder')
		.version('beta')
		.post({dateTimeTimeZone : snoozeReminder});
	console.log(res);
} catch (error) {
	throw error;
}

```