
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=')
		.filter('id eq 'String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color')')
		.expand('singleValueExtendedProperties')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```