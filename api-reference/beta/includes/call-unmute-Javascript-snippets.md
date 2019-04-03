
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const unmute = {
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/unmute')
	.version('beta')
	.post({String : unmute});

```