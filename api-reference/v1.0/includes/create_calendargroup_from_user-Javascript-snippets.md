
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calendarGroups = {
  name: "name-value",
  classId: "classId-value",
  changeKey: "changeKey-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/calendarGroups')
		.post({calendarGroup : calendarGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```