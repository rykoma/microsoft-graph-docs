
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const changeScreenSharingRole = {
  role: "viewer"
}
;

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/changeScreenSharingRole')
		.version('beta')
		.post({ScreenSharingRole : changeScreenSharingRole});
	console.log(res);
} catch (error) {
	throw error;
}

```