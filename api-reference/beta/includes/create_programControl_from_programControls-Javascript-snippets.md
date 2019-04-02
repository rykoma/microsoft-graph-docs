
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const programControls = {
    controlId: "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    controlTypeId: "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    programId: "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213"
};

//make the request to Graph
try{
	let res = await client.api('/programControls')
		.version('beta')
		.post({programControl : programControls});
	console.log(res);
} catch (error) {
	throw error;
}

```