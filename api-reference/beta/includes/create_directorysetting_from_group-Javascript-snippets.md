
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const settings = {
  directorySetting: {
    displayName: "displayName-value",
    templateId: "templateId-value",
    values: [
      {
        name: "name-value",
        value: "value-value"
      }
    ]
  }
};

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/settings')
		.version('beta')
		.post({directorySetting : settings});
	console.log(res);
} catch (error) {
	throw error;
}

```