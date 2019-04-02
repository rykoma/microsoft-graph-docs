
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const users = {
  accountEnabled: true,
  displayName: "displayName-value",
  mailNickname: "mailNickname-value",
  userPrincipalName: "upn-value@tenant-value.onmicrosoft.com",
  "passwordProfile" : {
    forceChangePasswordNextSignIn: true,
    password: "password-value"
  }
}
;

//make the request to Graph
try{
	let res = await client.api('/users')
		.post({user : users});
	console.log(res);
} catch (error) {
	throw error;
}

```