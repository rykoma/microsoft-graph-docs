
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
    emailAddresses:[
        {
            type:"personal",
            name:"Pavel Bansky",
            address:"pavelb@adatum.onmicrosoft.com"
        },
        {
          address: "pavelb@fabrikam.onmicrosoft.com",
          name: "Pavel Bansky",
          type: "other",
          otherLabel: "Volunteer work"
        }
    ]
};

//make the request to Graph
try{
	let res = await client.api('/me/contacts/AAMkADh6v5AAAvgTCEAAA=')
		.version('beta')
		.update({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```