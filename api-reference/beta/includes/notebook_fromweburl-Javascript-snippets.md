
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const GetNotebookFromWebUrl = {webUrl:"webUrl value"}
;

//make the request to Graph
try{
	let res = await client.api('/me/onenote/notebooks/GetNotebookFromWebUrl')
		.version('beta')
		.post({String : GetNotebookFromWebUrl});
	console.log(res);
} catch (error) {
	throw error;
}

```