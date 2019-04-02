
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/education/schools/2961761D-8094-4183-A9F6-8E36E966C7D9/administrativeUnit')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```