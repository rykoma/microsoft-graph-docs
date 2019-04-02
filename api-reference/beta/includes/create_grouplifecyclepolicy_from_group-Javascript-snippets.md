
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const groupLifecyclePolicies = {
  groupLifetimeInDays: 100,
  managedGroupTypes: "Selected",
  alternateNotificationEmails: "admin@contoso.com"
};

//make the request to Graph
try{
	let res = await client.api('/groupLifecyclePolicies')
		.version('beta')
		.post({groupLifecyclePolicy : groupLifecyclePolicies});
	console.log(res);
} catch (error) {
	throw error;
}

```