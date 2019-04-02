
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const reply = {
  post: {
    body: {
      contentType: "",
      content: "content-value"
    }
  }
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads/{id}/reply')
		.post({post : reply});
	console.log(res);
} catch (error) {
	throw error;
}

```