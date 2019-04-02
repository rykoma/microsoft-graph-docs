
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const appRoleAssignments = {
  creationTimestamp: "2016-10-19T10:37:00Z",
  principalDisplayName: "principalDisplayName-value",
  principalId: "principalId-value",
  principalType: "principalType-value",
  resourceDisplayName: "resourceDisplayName-value"
};

//make the request to Graph
try{
	let res = await client.api('/appRoleAssignments/{id}')
		.version('beta')
		.update({appRoleAssignment : appRoleAssignments});
	console.log(res);
} catch (error) {
	throw error;
}

```