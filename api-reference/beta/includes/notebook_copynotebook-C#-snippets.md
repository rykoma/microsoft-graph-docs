
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupId = "groupId-value";

var renameAs = "renameAs-value";

await graphClient.Me.Onenote.Notebooks["{id}"]
	.copyNotebook(groupId,renameAs,notebookFolder,siteCollectionId,siteId);
	.Request()
	.PostAsync()

```