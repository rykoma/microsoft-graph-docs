
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const mailFolders = {
  @odata.type: "microsoft.graph.mailSearchFolder",
  filterQuery: "contains(subject, 'Analytics')))"
};

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders/AAMkAGVmMDEzM')
		.version('beta')
		.update({mailFolder : mailFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```