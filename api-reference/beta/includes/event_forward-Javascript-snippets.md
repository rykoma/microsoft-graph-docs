
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const forward = {
  ToRecipients:[
      {
        emailAddress: {
          address:"danas@contoso.onmicrosoft.com",
          name:"Dana Swope"
        }
      }
     ],
  Comment: "Dana, hope you can make this meeting." 
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/forward')
		.version('beta')
		.post({String : forward});
	console.log(res);
} catch (error) {
	throw error;
}

```