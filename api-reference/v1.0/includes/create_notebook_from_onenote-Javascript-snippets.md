
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const notebooks = {
  displayName: "Notebook name"
};

//make the request to Graph
try{
	let res = await client.api('/me/onenote/notebooks')
		.post({notebook : notebooks});
	console.log(res);
} catch (error) {
	throw error;
}

```