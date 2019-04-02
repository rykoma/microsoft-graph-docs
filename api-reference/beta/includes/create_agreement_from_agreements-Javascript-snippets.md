
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const agreements = {
  displayName: "MSGraph Sample",
  isViewingBeforeAcceptanceRequired: true,
  files: [
    {
      fileName: "TOU.pdf",
      language: "en",
      isDefault: true,
      fileData: {
        data: "SGVsbG8gd29ybGQ="
      }
    }
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/agreements')
		.version('beta')
		.post({agreement : agreements});
	console.log(res);
} catch (error) {
	throw error;
}

```