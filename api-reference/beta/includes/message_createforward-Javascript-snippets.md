
```Javascript

const options = {
	authProvider,
};

//initialise the client
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

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADA1MTAAAH5JaLAAA=/createForward')
		.version('beta')
		.post({message : createForward});
	console.log(res);
} catch (error) {
	throw error;
}

```