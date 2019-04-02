
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMemberObjects = {
  securityEnabledOnly: true
}
;

//make the request to Graph
try{
	let res = await client.api('/directoryObjects/{object-id}/getMemberObjects')
		.post({Boolean : getMemberObjects});
	console.log(res);
} catch (error) {
	throw error;
}

```