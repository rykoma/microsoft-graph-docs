
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const updateAlerts = {
  value: [
    {
      assignedTo: "String",
      closedDateTime: "String (timestamp)",
      comments: ["String"],
      feedback: "@odata.type: microsoft.graph.alertFeedback",
      id: "String (identifier)",
      status: "@odata.type: microsoft.graph.alertStatus",
      tags: ["String"],
      vendorInformation:
        {
          provider: "String",
          vendor: "String"
        }
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/security/alerts/updateAlerts')
		.version('beta')
		.post({alert : updateAlerts});
	console.log(res);
} catch (error) {
	throw error;
}

```