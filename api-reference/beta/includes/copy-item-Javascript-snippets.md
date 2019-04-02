
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copy = {
  parentReference: {
    driveId: "6F7D00BF-FC4D-4E62-9769-6AEA81F3A21B",
    id: "DCD0D3AD-8989-4F23-A5A2-2C086050513F"
  },
  name: "contoso plan (copy).txt"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}/copy')
		.version('beta')
		.post({String : copy});
	console.log(res);
} catch (error) {
	throw error;
}

```