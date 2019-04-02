
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
    @odata.type: "#microsoft.graph.fileAttachment",
    name: "menu.txt",
    contentBytes: "bWFjIGFuZCBjaGVlc2UgdG9kYXk="
}
;

//make the request to Graph
try{
	let res = await client.api('/me/events('AAMkAGI1AAAt9AHjAAA=')/attachments')
		.version('beta')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```