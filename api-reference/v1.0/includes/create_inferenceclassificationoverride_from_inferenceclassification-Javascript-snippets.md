
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const overrides = {
  classifyAs: "focused",
  senderEmailAddress: {
    name: "Samantha Booth",
    address: "samanthab@adatum.onmicrosoft.com"
  }
}
;

//make the request to Graph
try{
	let res = await client.api('/me/inferenceClassification/overrides')
		.post({inferenceClassificationOverride : overrides});
	console.log(res);
} catch (error) {
	throw error;
}

```