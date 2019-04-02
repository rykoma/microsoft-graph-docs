
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const threads = {
  topic: "New Conversation Thread Topic",
  posts: [{
    body: {
      contentType: "html",
      content: "this is body content"
    },
    newParticipants: [{
      emailAddress: {
        name: "Alex Darrow",
        address: "alexd@contoso.com"
      }
    }]
  }]
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads')
		.version('beta')
		.post({conversationThread : threads});
	console.log(res);
} catch (error) {
	throw error;
}

```