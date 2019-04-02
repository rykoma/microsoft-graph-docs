
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
  receivedDateTime: "datetime-value",
  sentDateTime: "datetime-value",
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
		.post({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```