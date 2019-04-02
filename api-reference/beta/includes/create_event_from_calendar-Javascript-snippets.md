
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const events = {
  subject: "Let's go for lunch",
  body: {
    contentType: "HTML",
    content: "Does next month work for you?"
  },
  start: {
      dateTime: "2019-03-10T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2019-03-10T14:00:00",
      timeZone: "Pacific Standard Time"
  },
  location:{
      displayName:"Harry's Bar"
  },
  attendees: [
    {
      emailAddress: {
        address:"adelev@contoso.onmicrosoft.com",
        name: "Adele Vance"
      },
      type: "required"
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/me/calendars/AAMkAGViNDU7zAAAAAGtlAAA=/events')
		.version('beta')
		.post({event : events});
	console.log(res);
} catch (error) {
	throw error;
}

```