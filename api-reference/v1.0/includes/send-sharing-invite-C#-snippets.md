
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var email = "ryan@contoso.com";

var recipients = new List<Boolean>();
recipients.Add(new Boolean(email));

var message = "Here's the file that we're collaborating on.";

var requireSignIn = True;

var sendInvitation = True;

var roles = new List<Boolean>();

await graphClient.Me.Drive.Items["{item-id}"]
	.Invite(requireSignIn,roles,sendInvitation,message,recipients)
	.Request()
	.PostAsync()

```