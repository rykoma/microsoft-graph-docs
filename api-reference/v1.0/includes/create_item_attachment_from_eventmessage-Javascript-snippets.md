
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  @odata.type: "#Microsoft.OutlookServices.ItemAttachment",
  name: "name-value",
  item: "message or event entity"
};

//make the request to Graph
try{
	let res = await client.api('/me/events/{id}/attachments')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```