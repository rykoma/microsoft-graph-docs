
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const applications = {
  allowPublicClient: false,
  displayName: "New display name"
};

//make the request to Graph
try{
	let res = await client.api('/applications/{id}')
		.version('beta')
		.update({application : applications});
	console.log(res);
} catch (error) {
	throw error;
}

```