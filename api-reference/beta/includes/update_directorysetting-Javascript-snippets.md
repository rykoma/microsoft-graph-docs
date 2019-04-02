
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const settings = {
  values: [
    {
      name: "name-value",
      value: "value-value"
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/settings/{id}')
		.version('beta')
		.update({directorySetting : settings});
	console.log(res);
} catch (error) {
	throw error;
}

```