
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const move = {
  destinationId: "deleteditems"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADhAAATs28OAAA=/move')
		.version('beta')
		.post({String : move});
	console.log(res);
} catch (error) {
	throw error;
}

```