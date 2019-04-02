
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  givenName: "Pavel",
  surname: "Bansky",
  emailAddresses: [
    {
      address: "pavelb@contoso.onmicrosoft.com",
      name: "Pavel Bansky",
      type: "personal"
    },
    {
      address: "pavelb@fabrikam.onmicrosoft.com",
      name: "Pavel Bansky",
      type: "other",
      otherLabel: "Volunteer work"
    }
  ],
  "phones" : [
    {
      number: "+1 732 555 0102",
      type: "business"
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/me/contacts')
		.version('beta')
		.post({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```