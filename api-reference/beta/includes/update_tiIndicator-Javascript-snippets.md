
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tiIndicators = {
  additionalInformation: "additionalInformation-after-update",
  confidence: 42,
  description: "description-after-update",
};

//make the request to Graph
try{
	let res = await client.api('/security/tiIndicators/{id}')
		.version('beta')
		.update({tiIndicator : tiIndicators});
	console.log(res);
} catch (error) {
	throw error;
}

```