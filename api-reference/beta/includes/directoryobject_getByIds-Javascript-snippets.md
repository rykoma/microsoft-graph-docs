
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getByIds = {
    ids:["84b80893-8749-40a3-97b7-68513b600544","5d6059b6-368d-45f8-91e1-8e07d485f1d0"],
    types:["user"]
}
;

//make the request to Graph
try{
	let res = await client.api('/directoryObjects/getByIds')
		.version('beta')
		.post({String : getByIds});
	console.log(res);
} catch (error) {
	throw error;
}

```