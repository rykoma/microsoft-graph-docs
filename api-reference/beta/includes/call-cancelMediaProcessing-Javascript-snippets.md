
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const cancelMediaProcessing = {
  all: true,
  clientContext: "clientContext-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/cancelMediaProcessing')
		.version('beta')
		.post({Boolean : cancelMediaProcessing});
	console.log(res);
} catch (error) {
	throw error;
}

```