
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copy = {
  destinationId: "destinationId-value"
};

let res = await client.api('/me/messages/{id}/copy')
	.version('beta')
	.post({String : copy});

```