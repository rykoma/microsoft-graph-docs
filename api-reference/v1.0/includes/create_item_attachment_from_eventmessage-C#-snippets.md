
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of Attachment
var attachments = new Attachment
{
	@odata.type = "#Microsoft.OutlookServices.ItemAttachment",
	Name = "name-value",
	Item = "message or event entity",
};

await graphClient.Me.Events["{id}"].Attachments
	.Request()
	.AddAsync(attachments);

```