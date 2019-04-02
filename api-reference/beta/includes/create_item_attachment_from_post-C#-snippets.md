
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Item
var item = new Item
{
};

//create instance of Attachment
var attachments = new Attachment
{
	@odata.type = "#microsoft.graph.itemAttachment",
	Name = "name-value",
	Item = item,
};

await graphClient.Groups["{id}"].Threads["{id}"].Posts["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```