
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var toRecipients = new List<String>();
toRecipients.Add(new String(emailAddress));

await graphClient.Me.Messages["{id}"]
	.Forward(comment,toRecipients)
	.Request()
	.PostAsync()

```