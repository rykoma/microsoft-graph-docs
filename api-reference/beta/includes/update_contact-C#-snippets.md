
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var otherLabel = "Volunteer work";

var type = "other";

var name = "Pavel Bansky";

var address = "pavelb@fabrikam.onmicrosoft.com";

var addressVar = "pavelb@adatum.onmicrosoft.com";

var nameVar = "Pavel Bansky";

var typeVar = "personal";

//create TypedEmailAddress list and populate it
var emailAddresses = new List<TypedEmailAddress>();
emailAddresses.Add(new TypedEmailAddress(typeVar,nameVar,addressVar));
emailAddresses.Add(new TypedEmailAddress(address,name,type,otherLabel));

//create instance of Contact
var contacts = new Contact
{
	EmailAddresses = emailAddresses,
};

await graphClient.Me.Contacts["AAMkADh6v5AAAvgTCEAAA="]
	.Request()
	.UpdateAsync(contacts);

```