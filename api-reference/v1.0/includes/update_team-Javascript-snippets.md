
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const teams = {
  memberSettings: {
    allowCreateUpdateChannels: true
  },
  messagingSettings: {
    allowUserEditMessages: true,
    allowUserDeleteMessages: true
  },
  funSettings: {
    allowGiphy: true,
    giphyContentRating: "strict"
  }
};

//make the request to Graph
try{
	let res = await client.api('/teams/{id}')
		.update({team : teams});
	console.log(res);
} catch (error) {
	throw error;
}

```