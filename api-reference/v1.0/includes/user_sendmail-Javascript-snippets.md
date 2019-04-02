
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const sendMail = {
  message: {
    subject: "Meet for lunch?",
    body: {
      contentType: "Text",
      content: "The new cafeteria is open."
    },
    toRecipients: [
      {
        emailAddress: {
          address: "fannyd@contoso.onmicrosoft.com"
        }
      }
    ],
    ccRecipients: [
      {
        emailAddress: {
          address: "danas@contoso.onmicrosoft.com"
        }
      }
    ]
  },
  saveToSentItems: "false"
};

//make the request to Graph
try{
	let res = await client.api('/me/sendMail')
		.post({message : sendMail});
	console.log(res);
} catch (error) {
	throw error;
}

```