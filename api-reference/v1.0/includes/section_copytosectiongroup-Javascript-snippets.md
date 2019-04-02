
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copyToSectionGroup = {
  id: "id-value",
  groupId: "groupId-value",
  renameAs: "renameAs-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/sections/{id}/copyToSectionGroup')
		.post({String : copyToSectionGroup});
	console.log(res);
} catch (error) {
	throw error;
}

```