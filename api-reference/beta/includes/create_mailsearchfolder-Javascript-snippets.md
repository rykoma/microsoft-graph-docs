
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const childFolders = {
  @odata.type: "microsoft.graph.mailSearchFolder",
  displayName: "Get MyAnalytics",
  includeNestedFolders: true,
  sourceFolderIDs: ["AAMkAGVmMDEzM"],
  filterQuery: "contains(subject, 'MyAnalytics')"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders/searchfolders/childfolders')
		.version('beta')
		.post({mailFolder : childFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```