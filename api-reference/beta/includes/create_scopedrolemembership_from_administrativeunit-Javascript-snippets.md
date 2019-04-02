
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const scopedRoleMembers = {
  roleId: "roleId-value",
  roleMemberInfo: {
    id: "id-value"
  }
}
;

//make the request to Graph
try{
	let res = await client.api('/administrativeUnits/{id}/scopedRoleMembers')
		.version('beta')
		.post({scopedRoleMembership : scopedRoleMembers});
	console.log(res);
} catch (error) {
	throw error;
}

```