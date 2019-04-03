
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var emailAddress = new EmailAddress
{
	Address = "randiw@contoso.onmicrosoft.com",
	Name = "Randi Welch",
};

var emailAddressVar = new EmailAddress
{
	Address = "samanthab@contoso.onmicrosoft.com",
	Name = "Samantha Booth",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddressVar));
toRecipients.Add(new Recipient(emailAddress));

var message = new Message
{
	ToRecipients = toRecipients,
};

var comment = "Samantha, Randi, would you name the group please?";

await graphClient.Me.Messages["AAMkADA1MTAAAAqldOAAA="]
	.Reply(message,comment)
	.Request()
	.PostAsync()

```