
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const securityActions = {
  name: "BlockIp",
  actionReason: "Test",
  parameters: [
    {
      name: "IP",
      value: "1.2.3.4"
    }
  ],
  vendorInformation: {
    provider: "Windows Defender ATP",
    vendor: "Microsoft"
  }
};

//make the request to Graph
try{
	let res = await client.api('/security/securityActions')
		.version('beta')
		.post({securityAction : securityActions});
	console.log(res);
} catch (error) {
	throw error;
}

```