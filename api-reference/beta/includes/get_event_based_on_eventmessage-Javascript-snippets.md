
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages('AAMkADYAAAImV_jAAA=')')
	.version('beta')
	.expand('')
	.get();

```