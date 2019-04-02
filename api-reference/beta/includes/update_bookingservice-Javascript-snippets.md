
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const services = {
    @odata.type:"#microsoft.graph.bookingService",
    defaultDuration:"PT30M"
};

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/services/57da6774-a087-4d69-b0e6-6fb82c339976')
		.version('beta')
		.update({bookingService : services});
	console.log(res);
} catch (error) {
	throw error;
}

```