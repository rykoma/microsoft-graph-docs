
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of SecurityVendorInformation
var vendorInformation = new SecurityVendorInformation
{
	Provider = "String",
	Vendor = "String",
};

//create String list and populate it
var tags = new List<String>();

//create String list and populate it
var comments = new List<String>();

//create instance of Alert
var alerts = new Alert
{
	AssignedTo = "String",
	ClosedDateTime = "String (timestamp)",
	Comments = comments,
	Feedback = "@odata.type: microsoft.graph.alertFeedback",
	Status = "@odata.type: microsoft.graph.alertStatus",
	Tags = tags,
	VendorInformation = vendorInformation,
};

await graphClient.Security.Alerts["{alert_id}"]
	.Request()
	.UpdateAsync(alerts);

```