
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const cancel = {
  cancellationMessage: "Your appointment has been successfully cancelled. Please call us again."
}
;

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses/Contosolunchdelivery@M365B489948.onmicrosoft.com/appointments/AAMkADKoAAA=/cancel')
		.version('beta')
		.post({bookingAppointment : cancel});
	console.log(res);
} catch (error) {
	throw error;
}

```