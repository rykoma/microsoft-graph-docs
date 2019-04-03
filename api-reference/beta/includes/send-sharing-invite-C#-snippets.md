
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var email = "ryan@contoso.org";

var recipients = new List<Boolean>();
recipients.Add(new Boolean(email));

var message = "Here's the file that we're collaborating on.";

var requireSignIn = True;

var sendInvitation = True;

var roles = new List<Boolean>();

var password = "password123";

var expirationDateTime = 7/15/2018 2:00:00 PM;

await graphClient.Me.Drive.Items["{item-id}"]
	.Invite(requireSignIn,roles,sendInvitation,message,recipients,expirationDateTime,password)
	.Request()
	.PostAsync()

```