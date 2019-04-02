
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const invitations = {
  invitedUserEmailAddress: "yyy@test.com",
  inviteRedirectUrl: "https://myapp.com"
}
;

//make the request to Graph
try{
	let res = await client.api('/invitations')
		.version('beta')
		.post({invitation : invitations});
	console.log(res);
} catch (error) {
	throw error;
}

```