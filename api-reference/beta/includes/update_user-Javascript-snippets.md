
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const me = {
  accountEnabled: true,
  assignedLicenses: [
    {
      disabledPlans: [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ],
      skuId: "skuId-value"
    }
  ],
  assignedPlans: [
    {
      assignedDateTime: "2016-10-19T10:37:00Z",
      capabilityStatus: "capabilityStatus-value",
      service: "service-value",
      servicePlanId: "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  businessPhones: [
    "businessPhones-value"
  ],
  city: "city-value"
};

//make the request to Graph
try{
	let res = await client.api('/me')
		.version('beta')
		.update({user : me});
	console.log(res);
} catch (error) {
	throw error;
}

```