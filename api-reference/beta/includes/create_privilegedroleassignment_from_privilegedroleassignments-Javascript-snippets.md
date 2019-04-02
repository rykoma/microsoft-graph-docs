
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const privilegedRoleAssignments = {
  userId: "userId-value",
  roleId: "roleId-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/privilegedRoleAssignments')
		.version('beta')
		.post({privilegedRoleAssignment : privilegedRoleAssignments});
	console.log(res);
} catch (error) {
	throw error;
}

```