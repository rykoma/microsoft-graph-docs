
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const updateMetadata = {
  metadata: "metadata-value",
  clientContext: "clientContext-value"
};

let res = await client.api('/app/calls/{id}/updateMetadata')
	.version('beta')
	.post({String : updateMetadata});

```