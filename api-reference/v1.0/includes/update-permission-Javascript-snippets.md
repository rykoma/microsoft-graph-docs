
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const permissions = {
  roles: [ "read" ]
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}/permissions/{perm-id}')
		.update({permission : permissions});
	console.log(res);
} catch (error) {
	throw error;
}

```