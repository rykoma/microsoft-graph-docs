
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const translateExchangeIds = {
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  sourceIdType: "restId",
  targetIdType: "restImmutableEntryId"
};

//make the request to Graph
try{
	let res = await client.api('/me/translateExchangeIds')
		.version('beta')
		.post({String : translateExchangeIds});
	console.log(res);
} catch (error) {
	throw error;
}

```