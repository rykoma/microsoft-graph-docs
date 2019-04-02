
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const contacts = {
  homeAddress: {
    street: "123 Some street",
    city: "Seattle",
    state: "WA",
    postalCode: "98121"
  },
  birthday: "1974-07-22"
};

//make the request to Graph
try{
	let res = await client.api('/me/contacts/{id}')
		.update({contact : contacts});
	console.log(res);
} catch (error) {
	throw error;
}

```