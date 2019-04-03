
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var synchronizationTemplate = new SynchronizationTemplate
{
	Id = "SCIM-Test1",
	ApplicationId = "{id}",
	FactoryTag = "CustomSCIM",
};

await graphClient.Applications["{id}"].Synchronization.Templates
	.Request()
	.AddAsync(synchronizationTemplate);

```