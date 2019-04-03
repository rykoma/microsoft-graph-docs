
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "WA001";

var name = "x-custom-header-group-id";

var valueVar = "Washington";

var nameVar = "x-custom-header-group-nameVar";

var internetMessageHeaders = new List<InternetMessageHeader>();
internetMessageHeaders.Add(new InternetMessageHeader(nameVar,valueVar));
internetMessageHeaders.Add(new InternetMessageHeader(name,value));

var emailAddress = new EmailAddress
{
	Address = "AlexW@contoso.OnMicrosoft.com",
};

var toRecipients = new List<Recipient>();
toRecipients.Add(new Recipient(emailAddress));

var body = new ItemBody
{
	ContentType = "HTML",
	Content = "The group represents Washington.",
};

var message = new Message
{
	Subject = "9/8/2018: concert",
	Body = body,
	ToRecipients = toRecipients,
	InternetMessageHeaders = internetMessageHeaders,
};

await graphClient.Me.Messages
	.Request()
	.AddAsync(message);

```