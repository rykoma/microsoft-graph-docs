
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calendarGroups = {
  name: "name-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/calendarGroups/{id}')
		.version('beta')
		.update({calendarGroup : calendarGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```