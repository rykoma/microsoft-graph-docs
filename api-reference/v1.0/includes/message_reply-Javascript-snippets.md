
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const reply = {
  comment: "comment-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/{id}/reply')
		.post({String : reply});
	console.log(res);
} catch (error) {
	throw error;
}

```