
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const dismiss = Request Body
{
  userIds: [
    "04487ee0-f4f6-4e7f-8999-facc5a30e232",
    "13387ee0-f4f6-4e7f-8999-facc5120e345"
  ]
};

let res = await client.api('/riskyUsers/dismiss')
	.version('beta')
	.post({String : dismiss});

```