
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copy = {
  destinationId: "destinationId-value"
};

let res = await client.api('/me/mailFolders/{id}/copy')
	.post({String : copy});

```