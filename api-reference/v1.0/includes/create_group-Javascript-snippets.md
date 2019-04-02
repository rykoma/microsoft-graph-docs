
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const groups = {
  description: "Self help community for library",
  displayName: "Library Assist",
  groupTypes: [
    "Unified"
  ],
  mailEnabled: true,
  mailNickname: "library",
  securityEnabled: false
};

//make the request to Graph
try{
	let res = await client.api('/groups')
		.post({group : groups});
	console.log(res);
} catch (error) {
	throw error;
}

```