
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const customers = Content-type: application/json

{
    displayName: "Joni Sherman",
    emailAddress: "jonis@relecloud.com"
}
;

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/customers')
		.version('beta')
		.post({bookingCustomer : customers});
	console.log(res);
} catch (error) {
	throw error;
}

```