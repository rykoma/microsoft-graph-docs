
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const sendMail = {
  message: {
    subject: "9/9/2018: concert",
    body: {
      contentType: "HTML",
      content: "The group represents Nevada."
    },
    toRecipients: [
      {
        emailAddress: {
          address: "AlexW@contoso.OnMicrosoft.com"
        }
      }
    ],
    internetMessageHeaders:[
      {
        name:"x-custom-header-group-name",
        value:"Nevada"
      },
      {
        name:"x-custom-header-group-id",
        value:"NV001"
      }
    ]
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/sendMail')
		.version('beta')
		.post({message : sendMail});
	console.log(res);
} catch (error) {
	throw error;
}

```