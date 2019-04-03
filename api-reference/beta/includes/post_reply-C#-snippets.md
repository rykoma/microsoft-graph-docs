
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var id = "id-value";

var isInline = True;

var size = 99;

var contentType = "contentType-value";

var name = "name-value";

var lastModifiedDateTime = 10/19/2016 10:37:00 AM;

var attachments = new List<Attachment>();
attachments.Add(new Attachment(lastModifiedDateTime,name,contentType,size,isInline,id));

var inReplyTo = new Post
{
};

var categories = new List<String>();

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var newParticipants = new List<Recipient>();
newParticipants.Add(new Recipient(emailAddress));

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var sender = new Recipient
{
	EmailAddress = emailAddress,
};

var emailAddress = new EmailAddress
{
	Name = "name-value",
	Address = "address-value",
};

var from = new Recipient
{
	EmailAddress = emailAddress,
};

var body = new ItemBody
{
	ContentType = "",
	Content = "content-value",
};

var post = new Post
{
	Body = body,
	ReceivedDateTime = "2016-10-19T10:37:00Z",
	HasAttachments = true,
	From = from,
	Sender = sender,
	ConversationThreadId = "conversationThreadId-value",
	NewParticipants = newParticipants,
	ConversationId = "conversationId-value",
	CreatedDateTime = "2016-10-19T10:37:00Z",
	LastModifiedDateTime = "2016-10-19T10:37:00Z",
	ChangeKey = "changeKey-value",
	Categories = categories,
	Id = "id-value",
	InReplyTo = inReplyTo,
	Attachments = attachments,
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"]
	.Reply(post)
	.Request()
	.PostAsync()

```