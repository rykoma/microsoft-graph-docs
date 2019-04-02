
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
    content: "Does late morning work for you?"
  },
  start: {
      dateTime: "2017-04-15T12:00:00",
      timeZone: "Pacific Standard Time"
  },
  end: {
      dateTime: "2017-04-15T14:00:00",
      timeZone: "Pacific Standard Time"
  },
  location:{
      displayName:"Harry's Bar"
  },
  attendees: [
    {
      emailAddress: {
        address:"samanthab@contoso.onmicrosoft.com",
        name: "Samantha Booth"
      },
      type: "required"
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/me/events')
		.post({event : events});
	console.log(res);
} catch (error) {
	throw error;
}

```