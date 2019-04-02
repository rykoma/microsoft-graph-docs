
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  businessPhones: [
    "businessPhones-value"
  ],
  city: "city-value",
  companyName: "companyName-value",
  country: "country-value",
  department: "department-value",
  displayName: "displayName-value"
};

//make the request to Graph
try{
	let res = await client.api('/contacts/{id}')
		.version('beta')
		.update({orgContact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```