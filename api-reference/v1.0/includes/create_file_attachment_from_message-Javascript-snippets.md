
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  @odata.type: "#microsoft.graph.fileAttachment",
  name: "smile",
  contentBytes: "base64R0lGODdhEAYEAA7"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkpsDRVK/attachments')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```