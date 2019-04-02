
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  lastModifiedDateTime: "datetime-value",
  name: "name-value",
  contentType: "contentType-value",
  size: 99,
  isInline: true
};

//make the request to Graph
try{
	let res = await client.api('/users/{id}/outlook/tasks/{id}/attachments')
		.version('beta')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```