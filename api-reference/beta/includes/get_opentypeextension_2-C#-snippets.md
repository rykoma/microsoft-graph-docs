
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var extensions = await graphClient.Groups["f5480dfd-7d77-4d0b-ba2e-3391953cc74a"].Events["AAMkADVl17IsAAA="].Extensions["Com.Contoso.Deal"]
	.Request()
	.GetAsync();

```