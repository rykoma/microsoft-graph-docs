
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  @odata.type: "microsoft.graph.fileAttachment",
  name: "name-value",
  contentType: "contentType-value",
  isInline: false,
  contentLocation: "contentLocation-value",
  contentBytes: "base64-contentBytes-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/{id}/attachments')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```