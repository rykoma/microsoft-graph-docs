
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of DriveItem
var items = new DriveItem
{
	Name = "new-file-name.docx",
};

await graphClient.Me.Drive.Items["{item-id}"]
	.Request()
	.UpdateAsync(items);

```