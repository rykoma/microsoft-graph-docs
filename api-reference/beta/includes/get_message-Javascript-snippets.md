
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages('AAMkAGI1AAAoZCfHAAA=')')
	.version('beta')
	.get();

```