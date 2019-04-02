
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of MailFolder
var mailFolders = new MailFolder
{
	DisplayName = "displayName-value",
};

await graphClient.Me.MailFolders["AAMkAGVmMDEzM"]
	.Request()
	.UpdateAsync(mailFolders);

```