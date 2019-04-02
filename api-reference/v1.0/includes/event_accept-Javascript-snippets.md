
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const accept = {
  comment: "comment-value",
  sendResponse: true
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/accept')
		.post({String : accept});
	console.log(res);
} catch (error) {
	throw error;
}

```