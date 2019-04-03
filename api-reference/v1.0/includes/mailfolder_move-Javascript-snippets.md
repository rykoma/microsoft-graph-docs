
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const move = {
  destinationId: "destinationId-value"
};

let res = await client.api('/me/mailFolders/{id}/move')
	.post({String : move});

```