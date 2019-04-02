
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const assignments = {
  displayName: "Week 1 reading assignment",
  instructions: {
    contentType: "Text",
    content: "Read chapters 1 through 3"
  },
  dueDateTime: "2014-02-01T00:00:00Z"
};

//make the request to Graph
try{
	let res = await client.api('/education/classes/11021/assignments/19002')
		.version('beta')
		.update({educationAssignment : assignments});
	console.log(res);
} catch (error) {
	throw error;
}

```