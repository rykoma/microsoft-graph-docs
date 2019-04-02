
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const forward = {
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
  comment: "Dana, just want to make sure you get this." 
}
;

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADA1MTAAAH5JaLAAA=/forward')
		.version('beta')
		.post({message : forward});
	console.log(res);
} catch (error) {
	throw error;
}

```