
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/privilegedRoleAssignments/my')
	.version('beta')
	.get();

```