
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const agreements = {
  displayName: "displayName-value",
  isViewingBeforeAcceptanceRequired: true
};

//make the request to Graph
try{
	let res = await client.api('/agreements/'id'')
		.version('beta')
		.update({agreement : agreements});
	console.log(res);
} catch (error) {
	throw error;
}

```