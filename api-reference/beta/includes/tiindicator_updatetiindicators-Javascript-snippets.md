
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const updateTiIndicators = {
  value: [
    {
      id: "c6fb948b-89c5-3bba-a2cd-a9d9a1e430e4",
      additionalInformation: "mytest"
    },
    {
      id: "e58c072b-c9bb-a5c4-34ce-eb69af44fb1e",
      additionalInformation: "test again"
    }
  ]
}

;

//make the request to Graph
try{
	let res = await client.api('/security/tiIndicators/updateTiIndicators')
		.version('beta')
		.post({tiIndicator : updateTiIndicators});
	console.log(res);
} catch (error) {
	throw error;
}

```