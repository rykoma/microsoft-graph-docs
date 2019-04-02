
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const copyToSection = {
  id: "id-value",
  groupId: "groupId-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/pages/{id}/copyToSection')
		.post({String : copyToSection});
	console.log(res);
} catch (error) {
	throw error;
}

```