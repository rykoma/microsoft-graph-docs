
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```