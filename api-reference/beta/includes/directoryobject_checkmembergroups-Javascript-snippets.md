
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const checkMemberGroups = {
  groupIds: [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/me/checkMemberGroups')
		.post({String : checkMemberGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```