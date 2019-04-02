
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copyNotebook = {
  groupId: "groupId-value",
  renameAs: "renameAs-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/notebooks/{id}/copyNotebook')
		.version('beta')
		.post({String : copyNotebook});
	console.log(res);
} catch (error) {
	throw error;
}

```