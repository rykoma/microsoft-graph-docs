
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')')
	.version('beta')
	.filter('id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color')')
	.expand('singleValueExtendedProperties')
	.get();

```