
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var comment = "comment-value";

//create instance of EmailAddress
var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

//create String list and populate it
var toRecipients = new List<String>();
toRecipients.Add(new String(emailAddress));

await graphClient.Me.Messages["{id}"]
	.Forward(comment,toRecipients)
	.Request()
	.PostAsync()

```