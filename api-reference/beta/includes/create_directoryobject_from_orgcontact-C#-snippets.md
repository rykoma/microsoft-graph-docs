
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of DirectoryObject
var directoryObject = new DirectoryObject
{
};

//create instance of DirectoryObject
var memberOf = new DirectoryObject
{
	DirectoryObject = directoryObject,
};

await graphClient.Contacts["{id}"].MemberOf
	.Request()
	.AddAsync(memberOf);

```