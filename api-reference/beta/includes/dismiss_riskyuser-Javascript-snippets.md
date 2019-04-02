
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const dismiss = Request Body
{
  userIds: [
    "04487ee0-f4f6-4e7f-8999-facc5a30e232",
    "13387ee0-f4f6-4e7f-8999-facc5120e345"
  ]
};

//make the request to Graph
try{
	let res = await client.api('/riskyUsers/dismiss')
		.version('beta')
		.post({String : dismiss});
	console.log(res);
} catch (error) {
	throw error;
}

```