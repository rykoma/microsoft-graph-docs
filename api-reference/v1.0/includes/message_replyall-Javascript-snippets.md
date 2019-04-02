
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const replyAll = {
  comment: "comment-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/{id}/replyAll')
		.post({String : replyAll});
	console.log(res);
} catch (error) {
	throw error;
}

```