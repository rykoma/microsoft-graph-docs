
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
    @odata.type: "#microsoft.graph.referenceAttachment", 
    name: "Personal pictures", 
    sourceUrl: "https://contoso.com/personal/mario_contoso_net/Documents/Pics", 
    providerType: "oneDriveConsumer", 
    permission: "Edit", 
    isFolder: "True" 
} 
;

//make the request to Graph
try{
	let res = await client.api('/groups/c75831bdfad/threads/AAQkAGF97XEKhULw/posts/AAMkAGFcAAA/attachments')
		.version('beta')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```