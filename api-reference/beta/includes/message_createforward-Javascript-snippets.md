
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const createForward = {
  message:{  
    isDeliveryReceiptRequested: true,
    toRecipients:[
      {
        emailAddress: {
          address:"danas@contoso.onmicrosoft.com",
          name:"Dana Swope"
        }
      }
     ]
  },
  comment: "Dana, just want to make sure you get this; you'll need this if the project gets approved." 
};

let res = await client.api('/me/messages/AAMkADA1MTAAAH5JaLAAA=/createForward')
	.version('beta')
	.post({message : createForward});

```