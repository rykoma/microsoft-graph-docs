
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const taskFolders = {
  name: "Volunteer"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/outlook/taskfolders')
		.version('beta')
		.post({outlookTaskFolder : taskFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```