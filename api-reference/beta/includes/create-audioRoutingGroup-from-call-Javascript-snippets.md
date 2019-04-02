
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const audioRoutingGroups = {
  id: "oneToOne",
  routingMode: "oneToOne",
  sources: [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  receivers: [
    "550fae72-d251-43ec-868c-373732c2704f"
  ]
};

//make the request to Graph
try{
	let res = await client.api('/app/calls/{id}/audioRoutingGroups')
		.version('beta')
		.post({AudioRoutingGroup : audioRoutingGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```