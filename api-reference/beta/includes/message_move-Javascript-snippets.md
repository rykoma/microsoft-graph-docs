
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const move = {
  destinationId: "deleteditems"
};

let res = await client.api('/me/messages/AAMkADhAAATs28OAAA=/move')
	.version('beta')
	.post({String : move});

```