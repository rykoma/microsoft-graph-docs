
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const forceDelete = {
  disableUserAccounts: true
};

//make the request to Graph
try{
	let res = await client.api('/domains/{id}/forceDelete')
		.version('beta')
		.post({Boolean : forceDelete});
	console.log(res);
} catch (error) {
	throw error;
}

```