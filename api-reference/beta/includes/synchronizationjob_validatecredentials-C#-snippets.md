
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var value = "password-value";

var key = "Password";

var valueVar = "user@domain.com";

var keyVar = "UserName";

var credentials = new List<String>();
credentials.Add(new String(keyVar,valueVar));
credentials.Add(new String(key,value));

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{id}"]
	.ValidateCredentials(applicationIdentifier,templateId,useSavedCredentials,credentials)
	.Request()
	.PostAsync()

```