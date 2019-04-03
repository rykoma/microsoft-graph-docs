
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const accept = {
  comment: "comment-value",
  sendResponse: true
};

let res = await client.api('/me/events/{id}/accept')
	.version('beta')
	.post({String : accept});

```