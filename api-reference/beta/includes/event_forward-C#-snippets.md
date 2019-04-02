
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of EmailAddress
var emailAddress = new EmailAddress
{
	Address = "danas@contoso.onmicrosoft.com",
	Name = "Dana Swope",
};

//create String list and populate it
var ToRecipients = new List<String>();
ToRecipients.Add(new String(emailAddress));

var Comment = "Dana, hope you can make this meeting.";

await graphClient.Me.Events["{id}"]
	.Forward(comment,toRecipients)
	.Request()
	.PostAsync()

```