
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const users = {
  @odata.id:"https://graph.microsoft.com/v1.0/education/users/14008"
};

//make the request to Graph
try{
	let res = await client.api('/education/schools/{id}/users/$ref')
		.post({educationUser : users});
	console.log(res);
} catch (error) {
	throw error;
}

```