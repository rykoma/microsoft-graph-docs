
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const sections = {
  displayName: "Section name"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/notebooks/{id}/sections')
		.version('beta')
		.post({onenoteSection : sections});
	console.log(res);
} catch (error) {
	throw error;
}

```