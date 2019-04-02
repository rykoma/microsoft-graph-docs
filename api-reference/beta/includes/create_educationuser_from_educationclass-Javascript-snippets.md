
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const teachers = {
  @odata.id:"https://graph.microsoft.com/beta/education/users/14011"
};

//make the request to Graph
try{
	let res = await client.api('/education/classes/11017/teachers/$ref')
		.version('beta')
		.post({educationUser : teachers});
	console.log(res);
} catch (error) {
	throw error;
}

```