
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMemberGroups = {
  securityEnabledOnly: true
}
;

//make the request to Graph
try{
	let res = await client.api('/me/getMemberGroups')
		.post({Boolean : getMemberGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```