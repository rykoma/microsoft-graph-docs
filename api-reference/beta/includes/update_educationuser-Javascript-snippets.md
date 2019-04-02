
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const users = {
  displayName: "Rogelio Cazares",
  givenName: "Rogelio",
  middleName: "Fernando",
  surname: "Cazares",
};

//make the request to Graph
try{
	let res = await client.api('/education/users/13020')
		.version('beta')
		.update({educationUser : users});
	console.log(res);
} catch (error) {
	throw error;
}

```