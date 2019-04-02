
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const oAuth2Permissiongrants = {
  scope: "scope-value"
};

//make the request to Graph
try{
	let res = await client.api('/oAuth2Permissiongrants/{id}')
		.version('beta')
		.update({oAuth2PermissionGrant : oAuth2Permissiongrants});
	console.log(res);
} catch (error) {
	throw error;
}

```