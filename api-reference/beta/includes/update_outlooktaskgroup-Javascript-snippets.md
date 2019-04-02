
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const taskGroups = Content-type: application/json
Content-length: 28

{
  name: "Personal Tasks",
};

//make the request to Graph
try{
	let res = await client.api('/me/outlook/taskgroups('AAMkADIyAAAhrbe-AAA=')')
		.version('beta')
		.update({outlookTaskGroup : taskGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```