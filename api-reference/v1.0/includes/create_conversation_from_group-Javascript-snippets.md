
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const conversations = {
    topic:"New locations for this quarter",
    threads:[
        {
            posts:[
                {
                    body:{
                        contentType:"html",
                        content:"What do we know so far?"
                    },
                    newParticipants:[
                        {
                            emailAddress:{
                                name:"Adele Vance",
                                address:"AdeleV@contoso.onmicrosoft.com"
                            }
                        }
                    ]
                }
            ]
        }
    ]
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/29981b6a-0e57-42dc-94c9-cd24f5306196/conversations')
		.post({conversation : conversations});
	console.log(res);
} catch (error) {
	throw error;
}

```