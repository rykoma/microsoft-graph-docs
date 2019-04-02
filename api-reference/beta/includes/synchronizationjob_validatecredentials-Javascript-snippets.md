
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const validateCredentials = {
    credentials: [ 
        { key: "UserName", value: "user@domain.com" },
        { key: "Password", value: "password-value" }
    ]
}
;

//make the request to Graph
try{
	let res = await client.api('/servicePrincipals/{id}/synchronization/jobs/{id}/validateCredentials')
		.version('beta')
		.post({String : validateCredentials});
	console.log(res);
} catch (error) {
	throw error;
}

```