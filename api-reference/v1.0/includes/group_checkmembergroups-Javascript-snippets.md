
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const checkMemberGroups = {
  groupIds: [
    "groupIds-value"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/checkMemberGroups')
		.post({String : checkMemberGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```