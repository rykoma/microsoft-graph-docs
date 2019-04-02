
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messageRules = {
    displayName: "From partner",      
    sequence: 2,      
    isEnabled: true,          
    conditions: {
        senderContains: [
          "adele"       
        ]
     },
     actions: {
        forwardTo: [
          {
             emailAddress: {
                name: "Alex Wilbur",
                address: "AlexW@contoso.onmicrosoft.com"
              }
           }
        ],
        stopProcessingRules: true
     }    
};

//make the request to Graph
try{
	let res = await client.api('/me/mailFolders/inbox/messageRules')
		.post({messageRule : messageRules});
	console.log(res);
} catch (error) {
	throw error;
}

```