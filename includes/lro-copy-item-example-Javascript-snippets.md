
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copy = {
  parentReference: {
    path: "/drive/root:/Documents"
  },
  name: "Copy of LargeFolder1"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{folder-item-id}/copy')
		.version('beta')
		.post({String : copy});
	console.log(res);
} catch (error) {
	throw error;
}

```