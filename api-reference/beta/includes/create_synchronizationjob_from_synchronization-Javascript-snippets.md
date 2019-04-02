
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const jobs = {
    templateId: "BoxOutDelta"
}
;

//make the request to Graph
try{
	let res = await client.api('/servicePrincipals/{id}/synchronization/jobs')
		.version('beta')
		.post({synchronizationJob : jobs});
	console.log(res);
} catch (error) {
	throw error;
}

```