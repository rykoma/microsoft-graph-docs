
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "NV001";

var name = "x-custom-header-group-id";

var valueVar = "Nevada";

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
	Content = "The group represents Nevada.",
};

var message = new Message
{
	Subject = "9/9/2018: concert",
	Body = body,
	ToRecipients = toRecipients,
	InternetMessageHeaders = internetMessageHeaders,
};

await graphClient.Me
	.SendMail(message,saveToSentItems)
	.Request()
	.PostAsync()

```