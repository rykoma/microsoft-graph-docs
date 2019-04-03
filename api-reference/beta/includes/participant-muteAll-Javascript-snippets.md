
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const muteAll = {
  participants: [
    ""
  ],
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/participants/muteAll')
	.version('beta')
	.post({String : muteAll});

```