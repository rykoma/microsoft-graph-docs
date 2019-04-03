
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

var message = new Message
{
	ReceivedDateTime = "2016-10-19T10:37:00Z",
	SentDateTime = "2016-10-19T10:37:00Z",
	HasAttachments = true,
	Subject = "subject-value",
	Body = body,
	BodyPreview = "bodyPreview-value",
};

await graphClient.Me.MailFolders["{id}"].Messages
	.Request()
	.AddAsync(message);

```