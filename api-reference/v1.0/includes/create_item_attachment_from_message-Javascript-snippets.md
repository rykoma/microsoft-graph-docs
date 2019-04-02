
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const attachments = {
  @odata.type: "#microsoft.graph.itemAttachment",
  name: "Holiday event", 
  item: {
    @odata.type: "microsoft.graph.event",
    subject: "Discuss gifts for children",
    body: {
      contentType: "HTML",
      content: "Let's look for funding!"
    },
    start: {
      dateTime: "2016-12-02T18:00:00",
      timeZone: "Pacific Standard Time"
    },
    end: {
      dateTime: "2016-12-02T19:00:00",
      timeZone: "Pacific Standard Time"
    }
  }
};

//make the request to Graph
try{
	let res = await client.api('/me/messages/AAMkpsDRVK/attachments')
		.post({attachment : attachments});
	console.log(res);
} catch (error) {
	throw error;
}

```