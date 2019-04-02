
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
    subject:"Did you see last night's game?",
    importance:"Low",
    body:{
        contentType:"HTML",
        content:"They were <b>awesome</b>!"
    },
    toRecipients:[
        {
            emailAddress:{
                address:"AdeleV@contoso.onmicrosoft.com"
            }
        }
    ]
}
;

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