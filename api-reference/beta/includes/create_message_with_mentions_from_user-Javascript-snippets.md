
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
    subject: "Party planning",
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
};

//make the request to Graph
try{
	let res = await client.api('/me/messages')
		.version('beta')
		.post({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```