
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Item
var end = new Item
{
	DateTime = "2016-12-02T19:00:00",
	TimeZone = "Pacific Standard Time",
};

//create instance of Item
var start = new Item
{
	DateTime = "2016-12-02T18:00:00",
	TimeZone = "Pacific Standard Time",
};

//create instance of Item
var body = new Item
{
	ContentType = "HTML",
	Content = "Let's look for funding!",
};

//create instance of Item
var item = new Item
{
	@odata.type = "microsoft.graph.event",
	Subject = "Discuss gifts for children",
	Body = body,
	Start = start,
	End = end,
};

//create instance of Attachment
var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "Holiday event",
	Item = item,
};

await graphClient.Me.Messages["AAMkpsDRVK"].Attachments
	.Request()
	.AddAsync(attachments);

```