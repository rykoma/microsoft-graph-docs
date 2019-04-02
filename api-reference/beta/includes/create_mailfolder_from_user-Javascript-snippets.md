
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const mailFolders = {
  displayName: "displayName-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders')
		.version('beta')
		.post({mailFolder : mailFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```