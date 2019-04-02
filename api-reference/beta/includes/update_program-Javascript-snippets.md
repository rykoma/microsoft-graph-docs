
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const programs = {
    displayName: "testprogram3 new name"
};

//make the request to Graph
try{
	let res = await client.api('/programs('7e59d237-2fb0-4e5d-b7bb-d4f9f9129213')')
		.version('beta')
		.update({program : programs});
	console.log(res);
} catch (error) {
	throw error;
}

```