
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tasks = Prefer: outlook.timezone="Eastern Standard Time"
Content-type: application/json
Content-length: 76

{
  dueDateTime:  {
      dateTime: "2016-05-06T16:00:00",
      timeZone: "Eastern Standard Time"
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/outlook/tasks('AAMkADA1MTHgwAAA=')')
		.version('beta')
		.update({outlookTask : tasks});
	console.log(res);
} catch (error) {
	throw error;
}

```