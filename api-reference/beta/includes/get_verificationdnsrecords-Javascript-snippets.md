
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/domains/contoso.com/verificationDnsRecords')
	.version('beta')
	.get();

```