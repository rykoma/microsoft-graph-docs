
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const threads = {
  topic: "topic-value",
  posts: [{
      body: {
        contentType: "html",
        content: "this is body content"
      }
  }]
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/conversations/{id}/threads')
		.post({conversationThread : threads});
	console.log(res);
} catch (error) {
	throw error;
}

```