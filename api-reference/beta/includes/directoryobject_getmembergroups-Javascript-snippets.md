
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const String = {
  securityEnabledOnly: true
};

let res = await client.api('/me/getMemberGroups')
	.post({Boolean : String});

```