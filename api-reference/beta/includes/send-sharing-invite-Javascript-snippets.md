
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const invite = {
  recipients: [
    {
      email: "ryan@contoso.org"
    }
  ],
  message: "Here's the file that we're collaborating on.",
  requireSignIn: true,
  sendInvitation: true,
  roles: [ "write" ],
  password: "password123",
  expirationDateTime: "2018-07-15T14:00:00.000Z"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}/invite')
		.version('beta')
		.post({Boolean : invite});
	console.log(res);
} catch (error) {
	throw error;
}

```