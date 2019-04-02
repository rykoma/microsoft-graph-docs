
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const masterCategories = {
      displayName:"Project expenses",
      color:"preset9"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/outlook/masterCategories')
		.version('beta')
		.post({outlookCategory : masterCategories});
	console.log(res);
} catch (error) {
	throw error;
}

```