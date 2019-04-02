
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const createLink = {
  type: "embed"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}/createLink')
		.version('beta')
		.post({String : createLink});
	console.log(res);
} catch (error) {
	throw error;
}

```