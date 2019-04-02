
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const renewGroup = {
  groupId: "ffffffff-ffff-ffff-ffff-ffffffffffff"
};

//make the request to Graph
try{
	let res = await client.api('/groupLifecyclePolicies/renewGroup')
		.version('beta')
		.post({String : renewGroup});
	console.log(res);
} catch (error) {
	throw error;
}

```