
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const privilegedRoleAssignmentRequests = {
    duration: "2",
    reason: "Activate the role for business purpose",
    ticketNumber: "234",
    ticketSystem: "system",
    schedule: {
        startDateTime: "2018-02-08T02:35:17.903Z"
    },
    evaluateOnly: false,
    type: "UserAdd",
    assignmentState: "Active",
    roleId: "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
};

//make the request to Graph
try{
	let res = await client.api('/privilegedRoleAssignmentRequests')
		.version('beta')
		.post({privilegedRoleAssignmentRequest : privilegedRoleAssignmentRequests});
	console.log(res);
} catch (error) {
	throw error;
}

```