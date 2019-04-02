
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const templates = {
    id: "SCIM-Test1",
    applicationId: "{id}",
    factoryTag: "CustomSCIM"
};

//make the request to Graph
try{
	let res = await client.api('/applications/{id}/synchronization/templates')
		.version('beta')
		.post({synchronizationTemplate : templates});
	console.log(res);
} catch (error) {
	throw error;
}

```