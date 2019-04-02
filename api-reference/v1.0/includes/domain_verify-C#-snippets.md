
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Domains["{domain-name}"]
	.verify();
	.Request()
	.PostAsync()

```