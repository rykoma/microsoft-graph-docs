
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me
	.invalidateAllRefreshTokens();
	.Request()
	.PostAsync()

```