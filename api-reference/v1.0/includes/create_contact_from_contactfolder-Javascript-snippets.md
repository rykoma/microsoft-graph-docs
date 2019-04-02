
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  parentFolderId: "parentFolderId-value",
  birthday: "datetime-value",
  fileAs: "fileAs-value",
  displayName: "displayName-value",
  givenName: "givenName-value",
  initials: "initials-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/contactFolders/{id}/contacts')
		.post({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```