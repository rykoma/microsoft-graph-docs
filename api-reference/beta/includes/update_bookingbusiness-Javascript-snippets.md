
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const bookingBusinesses = {
  email: "admin@fabrikam.com",
  schedulingPolicy: {
      timeSlotInterval: "PT60M",
      minimumLeadTime: "P1D",
      maximumAdvance: "P30D",
      sendConfirmationsToOwner: true,
      allowStaffSelection: true
  }
};

//make the request to Graph
try{
	let res = await client.api('/bookingBusinesses/fabrikam@M365B489948.onmicrosoft.com')
		.version('beta')
		.update({bookingBusiness : bookingBusinesses});
	console.log(res);
} catch (error) {
	throw error;
}

```