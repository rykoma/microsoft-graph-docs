
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const answer = {
  callbackUri: "callbackUri-value",
  mediaConfig: {
    @odata.type: "#microsoft.graph.appHostedMediaConfig",
    blob: "<media config blob>"
  },
  acceptedModalities: [
    "audio"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/answer')
		.version('beta')
		.post({String : answer});
	console.log(res);
} catch (error) {
	throw error;
}

```