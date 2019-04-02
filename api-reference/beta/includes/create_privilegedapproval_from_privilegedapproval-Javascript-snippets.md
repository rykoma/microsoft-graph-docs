
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const privilegedApproval = {
  userId: "userId-value",
  roleId: "roleId-value",
  approvalType: "approvalType-value",
  approvalState: "approvalState-value",
  approvalDuration: "datetime-value"
};

//make the request to Graph
try{
	let res = await client.api('/privilegedApproval')
		.version('beta')
		.post({privilegedApproval : privilegedApproval});
	console.log(res);
} catch (error) {
	throw error;
}

```