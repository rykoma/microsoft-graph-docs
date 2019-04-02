
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const me = {
  accountEnabled: true,
  businessPhones: [
    "businessPhones-value"
  ],
  city: "city-value"
};

//make the request to Graph
try{
	let res = await client.api('/me')
		.update({user : me});
	console.log(res);
} catch (error) {
	throw error;
}

```