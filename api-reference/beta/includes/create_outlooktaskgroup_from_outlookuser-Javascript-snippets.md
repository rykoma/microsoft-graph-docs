
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const taskGroups = {
  name: "Leisure tasks"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/outlook/taskGroups')
		.version('beta')
		.post({outlookTaskGroup : taskGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```