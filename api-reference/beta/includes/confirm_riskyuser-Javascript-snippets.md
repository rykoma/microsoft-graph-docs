
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const confirmCompromised = 
Request Body
{
  userIds: [
    "29f270bb-4d23-4f68-8a57-dc73dc0d4caf",
    "20f91ec9-d140-4d90-9cd9-f618587a1471"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/riskyUsers/confirmCompromised')
		.version('beta')
		.post({String : confirmCompromised});
	console.log(res);
} catch (error) {
	throw error;
}

```