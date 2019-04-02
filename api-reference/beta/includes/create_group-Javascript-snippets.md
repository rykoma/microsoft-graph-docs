
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const groups = {
  description: "Self help community for golf",
  displayName: "Golf Assist",
  groupTypes: [
    "Unified"
  ],
  mailEnabled: true,
  mailNickname: "golfassist",
  securityEnabled: false
};

//make the request to Graph
try{
	let res = await client.api('/groups')
		.version('beta')
		.post({group : groups});
	console.log(res);
} catch (error) {
	throw error;
}

```