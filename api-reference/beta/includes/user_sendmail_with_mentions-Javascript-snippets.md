
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const sendMail = {
  Message: {
    subject: "Project kickoff",
    toRecipients:[
      {
          emailAddress:{
              name:"Samantha Booth",
              address:"samanthab@contoso.onmicrosoft.com"
          }
      }
    ],
    mentions:[
      {
        mentioned:{
          name:"Dana Swope",
          address:"danas@contoso.onmicrosoft.com"
         }
      }
    ]
  }
};

let res = await client.api('/me/sendMail')
	.version('beta')
	.post({message : sendMail});

```