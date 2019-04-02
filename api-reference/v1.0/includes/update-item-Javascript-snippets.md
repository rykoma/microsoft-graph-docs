
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const items = {
  name: "new-file-name.docx"
};

//make the request to Graph
try{
	let res = await client.api('/me/drive/items/{item-id}')
		.update({driveItem : items});
	console.log(res);
} catch (error) {
	throw error;
}

```