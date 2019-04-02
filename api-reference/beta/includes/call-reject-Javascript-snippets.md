
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const reject = {
  reason: "none"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/reject')
		.version('beta')
		.post({RejectReason : reject});
	console.log(res);
} catch (error) {
	throw error;
}

```