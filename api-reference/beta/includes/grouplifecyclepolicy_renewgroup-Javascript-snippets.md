
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const renewGroup = {
  groupId: "ffffffff-ffff-ffff-ffff-ffffffffffff"
};

let res = await client.api('/groupLifecyclePolicies/renewGroup')
	.version('beta')
	.post({String : renewGroup});

```