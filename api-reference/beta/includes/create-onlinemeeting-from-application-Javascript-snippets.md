
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const onlineMeetings = {
  meetingType: "meetNow",
  participants: {
    organizer: {
      identity: {
        user: {
          id: "550fae72-d251-43ec-868c-373732c2704f"
        }
      }
    }
  },
  subject: "subject-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/onlineMeetings')
		.version('beta')
		.post({OnlineMeeting : onlineMeetings});
	console.log(res);
} catch (error) {
	throw error;
}

```