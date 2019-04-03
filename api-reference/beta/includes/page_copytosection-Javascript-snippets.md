
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const copyToSection = {
  id: "id-value",
  groupId: "groupId-value"
};

let res = await client.api('/me/onenote/pages/{id}/copyToSection')
	.version('beta')
	.post({String : copyToSection});

```