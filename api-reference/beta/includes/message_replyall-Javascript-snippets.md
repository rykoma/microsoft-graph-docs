
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const replyAll = {
    message:{
      attachments: [ 
        { 
          @odata.type: "#microsoft.graph.fileAttachment", 
          name: "guidelines.txt", 
          contentBytes: "bWFjIGFuZCBjaGVlc2UgdG9kYXk=" 
        } 
      ]
    },
    comment: "Please take a look at the attached guidelines before you decide on the name." 
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkADA1MTAAAH5JaKAAA=/replyAll')
		.version('beta')
		.post({message : replyAll});
	console.log(res);
} catch (error) {
	throw error;
}

```