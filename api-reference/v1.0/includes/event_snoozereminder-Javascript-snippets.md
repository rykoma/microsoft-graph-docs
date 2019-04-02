
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const snoozeReminder = {
  newReminderTime: {
    dateTime: "dateTime-value",
    timeZone: "timeZone-value"
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/snoozeReminder')
		.post({dateTimeTimeZone : snoozeReminder});
	console.log(res);
} catch (error) {
	throw error;
}

```