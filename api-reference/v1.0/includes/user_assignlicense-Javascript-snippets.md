
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const assignLicense = {
  addLicenses: [
    {
      disabledPlans: [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      skuId: "guid"
    }
  ],
  removeLicenses: [ "bea13e0c-3828-4daa-a392-28af7ff61a0f" ]
};

//make the request to Graph
try{
	let res = await client.api('/me/assignLicense')
		.post({assignedLicense : assignLicense});
	console.log(res);
} catch (error) {
	throw error;
}

```