
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const applications = {
  allowPublicClient: true,
  displayName: "Display name"
};

//make the request to Graph
try{
	let res = await client.api('/applications')
		.version('beta')
		.post({application : applications});
	console.log(res);
} catch (error) {
	throw error;
}

```