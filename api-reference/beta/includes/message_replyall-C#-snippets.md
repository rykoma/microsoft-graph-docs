
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var contentBytes = "bWFjIGFuZCBjaGVlc2UgdG9kYXk=";

var name = "guidelines.txt";

var @odata.type = "#microsoft.graph.fileAttachment";

var attachments = new List<Attachment>();
attachments.Add(new Attachment(@odata.type,name,contentBytes));

var message = new Message
{
	Attachments = attachments,
};

var comment = "Please take a look at the attached guidelines before you decide on the name.";

await graphClient.Me.Messages["AAMkADA1MTAAAH5JaKAAA="]
	.ReplyAll(message,comment)
	.Request()
	.PostAsync()

```