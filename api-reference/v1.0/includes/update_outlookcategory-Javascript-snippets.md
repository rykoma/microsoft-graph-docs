
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const masterCategories = {
  color:"preset15"
};

//make the request to Graph
try{
	let res = await client.api('/me/outlook/masterCategories/bac262b7-485d-4739-b436-e31467d64fac')
		.update({outlookCategory : masterCategories});
	console.log(res);
} catch (error) {
	throw error;
}

```