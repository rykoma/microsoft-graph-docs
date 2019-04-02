
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMemberGroups = {
  securityEnabledOnly: false
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/getMemberGroups')
		.post({Boolean : getMemberGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```