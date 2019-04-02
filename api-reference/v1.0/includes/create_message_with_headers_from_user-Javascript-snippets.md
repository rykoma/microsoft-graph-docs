
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
    subject:"9/8/2018: concert",
    body:{
        contentType:"HTML",
        content:"The group represents Washington."
    },
    toRecipients:[
        {
            emailAddress:{
                address:"AlexW@contoso.OnMicrosoft.com"
            }
        }
    ],
    internetMessageHeaders:[
        {
            name:"x-custom-header-group-name",
            value:"Washington"
        },
        {
            name:"x-custom-header-group-id",
            value:"WA001"
        }
    ]
};

//make the request to Graph
try{
	let res = await client.api('/me/messages')
		.post({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```