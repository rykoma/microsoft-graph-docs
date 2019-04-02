
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contactFolders = {
  parentFolderId: "parentFolderId-value",
  displayName: "displayName-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/contactFolders')
		.post({contactFolder : contactFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```