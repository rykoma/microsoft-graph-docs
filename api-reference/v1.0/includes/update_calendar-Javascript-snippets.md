
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const calendar = {
  name: "Social events"
};

//make the request to Graph
try{
	let res = await client.api('/me/calendar')
		.update({calendar : calendar});
	console.log(res);
} catch (error) {
	throw error;
}

```