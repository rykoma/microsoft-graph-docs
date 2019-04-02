
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const childFolders = {
  displayName: "displayName-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/contactFolders/{id}/childFolders')
		.version('beta')
		.post({contactFolder : childFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```