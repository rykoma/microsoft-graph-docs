
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const subscriptions = {
   changeType: "created,updated",
   notificationUrl: "https://webhook.azurewebsites.net/api/send/myNotifyClient",
   resource: "me/mailFolders('Inbox')/messages",
   expirationDateTime:"2016-11-20T18:23:45.9356913Z",
   clientState: "secretClientValue"
};

//make the request to Graph
try{
	let res = await client.api('/subscriptions')
		.post({subscription : subscriptions});
	console.log(res);
} catch (error) {
	throw error;
}

```