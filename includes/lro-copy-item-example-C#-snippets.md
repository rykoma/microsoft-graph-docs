
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var parentReference = new String
{
	Path = "/drive/root:/Documents",
};

var name = "Copy of LargeFolder1";

await graphClient.Me.Drive.Items["{folder-item-id}"]
	.Copy(name,parentReference)
	.Request()
	.PostAsync()

```