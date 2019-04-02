
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  givenName: "Pavel",
  surname: "Bansky",
  emailAddresses: [
    {
      address: "pavelb@fabrikam.onmicrosoft.com",
      name: "Pavel Bansky"
    }
  ],
  businessPhones: [
    "+1 732 555 0102"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/me/contacts')
		.post({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```