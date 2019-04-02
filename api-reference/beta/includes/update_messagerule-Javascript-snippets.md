
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messageRules = Content-type: application/json

{
    displayName: "Important from partner",
    actions: {
        markImportance: "high"
     }
};

//make the request to Graph
try{
	let res = await client.api('/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')')
		.version('beta')
		.update({messageRule : messageRules});
	console.log(res);
} catch (error) {
	throw error;
}

```