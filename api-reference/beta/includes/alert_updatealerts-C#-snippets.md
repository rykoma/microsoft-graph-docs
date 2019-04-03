
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var vendorInformation = new SecurityVendorInformation
{
	Provider = "String",
	Vendor = "String",
};

var tags = new List<String>();

var status = "@odata.type: microsoft.graph.alertStatus";

var id = "String (identifier)";

var feedback = "@odata.type: microsoft.graph.alertFeedback";

var comments = new List<String>();

var closedDateTime = "String (timestamp)";

var assignedTo = "String";

var value = new List<Alert>();
value.Add(new Alert(assignedTo,closedDateTime,comments,feedback,id,status,tags,vendorInformation));

await graphClient.Security.Alerts
	.UpdateAlerts(value)
	.Request()
	.PostAsync()

```