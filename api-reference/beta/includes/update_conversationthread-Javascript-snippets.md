
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const threads = {
  @odata.type:"#Microsoft.OutlookServices.ConversationThread",
  isLocked: true
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads/{id}')
		.version('beta')
		.update({conversationThread : threads});
	console.log(res);
} catch (error) {
	throw error;
}

```