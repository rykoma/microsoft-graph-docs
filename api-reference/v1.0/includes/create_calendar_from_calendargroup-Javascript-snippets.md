
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calendars = {
  name: "name-value",
  color: {
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/calendarGroups/{id}/calendars')
		.post({calendar : calendars});
	console.log(res);
} catch (error) {
	throw error;
}

```