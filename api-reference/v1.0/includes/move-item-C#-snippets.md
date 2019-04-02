
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of ParentReference
var parentReference = new ParentReference
{
	Id = "{new-parent-folder-id}",
};

//create instance of DriveItem
var items = new DriveItem
{
	ParentReference = parentReference,
	Name = "new-item-name.txt",
};

await graphClient.Me.Drive.Items["{item-id}"]
	.Request()
	.UpdateAsync(items);

```