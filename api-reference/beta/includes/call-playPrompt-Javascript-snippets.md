
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const playPrompt = {
  clientContext: "d45324c1-fcb5-430a-902c-f20af696537c",
  prompts: [
    {
      @odata.type: "#microsoft.graph.mediaPrompt",
      mediaInfo: {
        uri: "https://cdn.contoso.com/beep.wav",
        resourceId: "1D6DE2D4-CD51-4309-8DAA-70768651088E"
      },
      loop: 5
    }
  ]
};

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/playPrompt')
		.version('beta')
		.post({Prompt : playPrompt});
	console.log(res);
} catch (error) {
	throw error;
}

```