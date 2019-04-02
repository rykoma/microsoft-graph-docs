
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const exportPersonalData = {
  storageLocation: "storageLocation-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/users/{id}/exportPersonalData')
		.post({String : exportPersonalData});
	console.log(res);
} catch (error) {
	throw error;
}

```