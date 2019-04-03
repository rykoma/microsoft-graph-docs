
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const mute = {
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/participants/{id}/mute')
	.version('beta')
	.post({String : mute});

```