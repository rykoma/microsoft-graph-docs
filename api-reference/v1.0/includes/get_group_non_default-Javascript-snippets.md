
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/groups/b320ee12-b1cd-4cca-b648-a437be61c5cd')
		.select('allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```