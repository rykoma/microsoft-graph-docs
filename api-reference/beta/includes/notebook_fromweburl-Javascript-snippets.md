
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const GetNotebookFromWebUrl = {webUrl:"webUrl value"};

let res = await client.api('/me/onenote/notebooks/GetNotebookFromWebUrl')
	.version('beta')
	.post({String : GetNotebookFromWebUrl});

```