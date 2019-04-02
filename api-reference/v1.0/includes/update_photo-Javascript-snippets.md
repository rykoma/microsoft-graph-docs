
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const photo = {
  height: 99,
  width: 99,
  id: "id-value"
};

//make the request to Graph
try{
	let res = await client.api('/users/{id|userPrincipalName}/photo')
		.update({profilePhoto : photo});
	console.log(res);
} catch (error) {
	throw error;
}

```