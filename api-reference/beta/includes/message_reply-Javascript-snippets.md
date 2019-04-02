
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const reply = {
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
  comment: "Samantha, Randi, would you name the group please?" 
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADA1MTAAAAqldOAAA=/reply')
		.version('beta')
		.post({message : reply});
	console.log(res);
} catch (error) {
	throw error;
}

```