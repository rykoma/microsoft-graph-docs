
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var businessPhones = new List<String>();

var name = "Pavel Bansky";

var address = "pavelb@fabrikam.onmicrosoft.com";

var emailAddresses = new List<EmailAddress>();
emailAddresses.Add(new EmailAddress(address,name));

var contact = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	BusinessPhones = businessPhones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contact);

```