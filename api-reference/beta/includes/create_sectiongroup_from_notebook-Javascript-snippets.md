
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const sectionGroups = {
  displayName: "Section group name"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/notebooks/{id}/sectionGroups')
		.version('beta')
		.post({sectionGroup : sectionGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```