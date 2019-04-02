
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const taskFolders = {
  name: "Charity work"
};

//make the request to Graph
try{
	let res = await client.api('/me/outlook/taskFolders('AAMkADIyAAAhrbPWAAA=')')
		.version('beta')
		.update({outlookTaskFolder : taskFolders});
	console.log(res);
} catch (error) {
	throw error;
}

```