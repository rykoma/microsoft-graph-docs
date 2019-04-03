
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const reject = {
  reason: "none"
};

let res = await client.api('/app/calls/{id}/reject')
	.version('beta')
	.post({RejectReason : reject});

```