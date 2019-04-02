
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const schemaExtensions = {
  properties: [
    {
      name:"new-name-value",
      type:"new-type-value"
    },
    {
      name:"additional-name-value",
      type:"additional-type-value"
    }
  ],
};

//make the request to Graph
try{
	let res = await client.api('/schemaExtensions/{id}')
		.version('beta')
		.update({schemaExtension : schemaExtensions});
	console.log(res);
} catch (error) {
	throw error;
}

```