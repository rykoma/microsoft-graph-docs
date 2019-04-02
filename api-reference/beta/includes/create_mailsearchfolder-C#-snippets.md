
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create SourceFolderIDs list and populate it
var sourceFolderIDs = new List<SourceFolderIDs>();

//create instance of MailFolder
var childFolders = new MailFolder
{
	@odata.type = "microsoft.graph.mailSearchFolder",
	DisplayName = "Get MyAnalytics",
	IncludeNestedFolders = true,
	SourceFolderIDs = sourceFolderIDs,
	FilterQuery = "contains(subject, 'MyAnalytics')",
};

await graphClient.Me.MailFolders["searchfolders"].ChildFolders
	.Request()
	.AddAsync(childFolders);

```