
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new Attachment
{
	@odata.type = "microsoft.graph.fileAttachment",
	Name = "name-value",
	ContentType = "contentType-value",
	IsInline = false,
	ContentLocation = "contentLocation-value",
	ContentBytes = "base64-contentBytes-value",
};

await graphClient.Me.Messages["{id}"].Attachments
	.Request()
	.AddAsync(attachment);

```