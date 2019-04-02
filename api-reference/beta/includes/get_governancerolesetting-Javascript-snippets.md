
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/privilegedAccess/azureResources/roleSettings/80dc5d6f-8d89-47b3-953f-01dc909ed3f9')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```