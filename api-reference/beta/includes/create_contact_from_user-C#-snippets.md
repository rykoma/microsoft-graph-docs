
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var type = "business";

var number = "+1 732 555 0102";

var phones = new List<Phone>();
phones.Add(new Phone(number,type));

var otherLabel = "Volunteer work";

var type = "other";

var name = "Pavel Bansky";

var address = "pavelb@fabrikam.onmicrosoft.com";

var typeVar = "personal";

var nameVar = "Pavel Bansky";

var addressVar = "pavelb@contoso.onmicrosoft.com";

var emailAddresses = new List<TypedEmailAddress>();
emailAddresses.Add(new TypedEmailAddress(addressVar,nameVar,typeVar));
emailAddresses.Add(new TypedEmailAddress(address,name,type,otherLabel));

var contact = new Contact
{
	GivenName = "Pavel",
	Surname = "Bansky",
	EmailAddresses = emailAddresses,
	Phones = phones,
};

await graphClient.Me.Contacts
	.Request()
	.AddAsync(contact);

```