
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const checkin = {
  comment: "Updating the latest guidelines"
};

//make the request to Graph
try{
	let res = await client.api('/drives/{drive-id}/items/{item-id}/checkin')
		.version('beta')
		.post({String : checkin});
	console.log(res);
} catch (error) {
	throw error;
}

```