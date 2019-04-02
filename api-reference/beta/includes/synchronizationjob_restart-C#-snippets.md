
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

//create instance of SynchronizationJobRestartCriteria
var criteria = new SynchronizationJobRestartCriteria
{
	ResetScope = "ConnectorDataStore, Escrows, QuarantineState",
};

await graphClient.ServicePrincipals["{id}"].Synchronization.Jobs["{jobId}"]
	.Restart(criteria)
	.Request()
	.PostAsync()

```