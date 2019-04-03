
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new Attachment
{
	@odata.type = "#microsoft.graph.fileAttachment",
	Name = "smile",
	ContentBytes = "R0lGODdhEAYEAA7",
};

await graphClient.Me.Messages["AAMkpsDRVK"].Attachments
	.Request()
	.AddAsync(attachment);

```