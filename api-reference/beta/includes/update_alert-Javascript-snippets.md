
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const alerts = {
  assignedTo: "String",
  closedDateTime: "String (timestamp)",
  comments: ["String"],
  feedback: "@odata.type: microsoft.graph.alertFeedback",
  status: "@odata.type: microsoft.graph.alertStatus",
  tags: ["String"],
  vendorInformation:
    {
      provider: "String",
      vendor: "String"
    }
};

//make the request to Graph
try{
	let res = await client.api('/security/alerts/{alert_id}')
		.version('beta')
		.update({alert : alerts});
	console.log(res);
} catch (error) {
	throw error;
}

```