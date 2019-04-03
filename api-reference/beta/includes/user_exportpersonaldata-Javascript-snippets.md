
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const exportPersonalData = {
  storageLocation: "storageLocation-value"
};

let res = await client.api('/users/{id}/exportPersonalData')
	.version('beta')
	.post({String : exportPersonalData});

```