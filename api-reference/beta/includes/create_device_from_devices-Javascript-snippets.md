
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const devices = {
  accountEnabled: true,
  alternativeSecurityIds: [
    {
      type: 99,
      identityProvider: "identityProvider-value",
      key: "key-value"
    }
  ],
  approximateLastSignInDateTime: "2016-10-19T10:37:00Z",
  deviceId: "deviceId-value",
  deviceMetadata: "deviceMetadata-value",
  deviceVersion: 99
};

//make the request to Graph
try{
	let res = await client.api('/devices')
		.version('beta')
		.post({device : devices});
	console.log(res);
} catch (error) {
	throw error;
}

```