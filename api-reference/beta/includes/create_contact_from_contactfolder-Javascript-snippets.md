
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  parentFolderId: "parentFolderId-value",
  birthday: "2016-10-19T10:37:00Z",
  fileAs: "fileAs-value",
  displayName: "displayName-value",
  givenName: "givenName-value",
  initials: "initials-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/contactFolders/{id}/contacts')
		.version('beta')
		.post({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```