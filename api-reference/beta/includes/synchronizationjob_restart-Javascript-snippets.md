
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const restart = {
   criteria: {
       resetScope: "ConnectorDataStore, Escrows, QuarantineState"
   }
}
;

//make the request to Graph
try{
	let res = await client.api('/servicePrincipals/{id}/synchronization/jobs/{jobId}/restart')
		.version('beta')
		.post({synchronizationJobRestartCriteria : restart});
	console.log(res);
} catch (error) {
	throw error;
}

```