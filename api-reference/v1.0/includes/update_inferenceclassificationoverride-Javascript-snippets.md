
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const overrides = {
  classifyAs: "focused"
};

//make the request to Graph
try{
	let res = await client.api('/me/inferenceClassification/overrides/{id}')
		.update({inferenceClassificationOverride : overrides});
	console.log(res);
} catch (error) {
	throw error;
}

```