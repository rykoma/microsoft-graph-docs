
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const createReply = {
  message:{  
    toRecipients:[
      {
        emailAddress: {
          address:"samanthab@contoso.onmicrosoft.com",
          name:"Samantha Booth"
        }
      },
      {
        emailAddress:{
          address:"randiw@contoso.onmicrosoft.com",
          name:"Randi Welch"
        }
      }
     ]
  },
  comment: "Samantha, Randi, would you name the group if the project is approved, please?" 
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADA1MTAAAAqldOAAA=/createReply')
		.version('beta')
		.post({message : createReply});
	console.log(res);
} catch (error) {
	throw error;
}

```