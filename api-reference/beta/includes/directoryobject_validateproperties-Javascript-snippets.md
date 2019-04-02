
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const validateProperties = {
  entityType: "Group",
  displayName: "Myprefix_test_mysuffix",
  mailNickname: "Myprefix_test_mysuffix",
  onBehalfOfUserId: "onBehalfOfUserId-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/directoryObjects/validateProperties')
		.version('beta')
		.post({String : validateProperties});
	console.log(res);
} catch (error) {
	throw error;
}

```