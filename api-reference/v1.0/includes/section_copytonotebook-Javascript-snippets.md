
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copyToNotebook = {
  id: "id-value",
  groupId: "groupId-value",
  renameAs: "renameAs-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/onenote/sections/{id}/copyToNotebook')
		.post({String : copyToNotebook});
	console.log(res);
} catch (error) {
	throw error;
}

```