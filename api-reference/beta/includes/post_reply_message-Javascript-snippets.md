
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const replies = {
  body: {
    contentType: "html",
    content: "Hello World"
  }
};

//make the request to Graph
try{
	let res = await client.api('/teams/{id}/channels/{id}/messages/{id}/replies')
		.version('beta')
		.post({chatMessage : replies});
	console.log(res);
} catch (error) {
	throw error;
}

```