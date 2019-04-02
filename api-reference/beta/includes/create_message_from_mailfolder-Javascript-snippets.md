
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
  receivedDateTime: "2016-10-19T10:37:00Z",
  sentDateTime: "2016-10-19T10:37:00Z",
  hasAttachments: true,
  subject: "subject-value",
  body: {
    contentType: "",
    content: "content-value"
  },
  bodyPreview: "bodyPreview-value"
};

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders/{id}/messages')
		.version('beta')
		.post({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```