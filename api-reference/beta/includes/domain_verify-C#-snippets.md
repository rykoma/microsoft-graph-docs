
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Domains["contoso.com"]
	.verify();
	.Request()
	.PostAsync()

```