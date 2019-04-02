
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const children = {
  name: "New Folder",
  folder: { },
  @microsoft.graph.conflictBehavior: "rename"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/root/children')
		.post({driveItem : children});
	console.log(res);
} catch (error) {
	throw error;
}

```