
```Javascript

const options = {
	authProvider,
};

//initialise the client
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