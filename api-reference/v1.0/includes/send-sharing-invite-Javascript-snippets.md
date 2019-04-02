
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const invite = {
  recipients: [
    {
      email: "ryan@contoso.com"
    }
  ],
  message: "Here's the file that we're collaborating on.",
  requireSignIn: true,
  sendInvitation: true,
  roles: [ "write" ]
}
;

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}/invite')
		.post({Boolean : invite});
	console.log(res);
} catch (error) {
	throw error;
}

```