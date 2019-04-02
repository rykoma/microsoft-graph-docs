
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  @odata.type: "#microsoft.graph.itemAttachment",
  name: "name-value",
  item: { }
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads/{id}/posts/{id}/attachments')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```