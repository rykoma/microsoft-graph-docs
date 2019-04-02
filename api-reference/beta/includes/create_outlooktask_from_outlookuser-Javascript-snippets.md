
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tasks = {
  assignedTo: "Dana Swope",
  subject: "Shop for children's weekend",
  startDateTime: {
      dateTime: "2016-05-03T09:00:00",
      timeZone: "Eastern Standard Time"
  },
  dueDateTime:  {
      dateTime: "2016-05-05T16:00:00",
      timeZone: "Eastern Standard Time"
  }
}
;

//make the request to Graph
try{
	let res = await client.api('/me/outlook/tasks')
		.version('beta')
		.post({outlookTask : tasks});
	console.log(res);
} catch (error) {
	throw error;
}

```