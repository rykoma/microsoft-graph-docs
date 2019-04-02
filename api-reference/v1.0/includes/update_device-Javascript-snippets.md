
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const devices = {
  accountEnabled: false
};

//make the request to Graph
try{
	let res = await client.api('/devices/{id}')
		.update({device : devices});
	console.log(res);
} catch (error) {
	throw error;
}

```