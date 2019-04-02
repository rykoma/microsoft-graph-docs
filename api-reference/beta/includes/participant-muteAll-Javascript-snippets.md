
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const muteAll = {
  participants: [
    ""
  ],
  clientContext: "clientContext-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/participants/muteAll')
		.version('beta')
		.post({String : muteAll});
	console.log(res);
} catch (error) {
	throw error;
}

```