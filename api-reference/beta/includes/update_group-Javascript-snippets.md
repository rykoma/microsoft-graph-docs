
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const groups = {
  description: "description-value",
  displayName: "displayName-value",
  groupTypes: [
    "groupTypes-value"
  ],
  mail: "mail-value",
  mailEnabled: true,
  mailNickname: "mailNickname-value"
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}')
		.version('beta')
		.update({group : groups});
	console.log(res);
} catch (error) {
	throw error;
}

```