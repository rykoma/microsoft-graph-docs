
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const validateProperties = {
  displayName: "Myprefix_test_mysuffix",
  mailNickname: "Myprefix_test_mysuffix",
  onBehalfOfUserId: "onBehalfOfUserId-value"
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/validateProperties')
		.version('beta')
		.post({String : validateProperties});
	console.log(res);
} catch (error) {
	throw error;
}

```