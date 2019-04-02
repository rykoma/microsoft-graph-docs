
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const classes = {
  description: "History - World History 1",
  displayName: "World History Level 1",
};

//make the request to Graph
try{
	let res = await client.api('/education/classes/{class-id}')
		.update({educationClass : classes});
	console.log(res);
} catch (error) {
	throw error;
}

```