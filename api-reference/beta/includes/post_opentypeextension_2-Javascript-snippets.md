
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const extensions = {
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "extensionName" : "Com.Contoso.Referral",
  "companyName" : "Wingtip Toys",
  "dealValue" : 500050,
  "expirationDate" : "2015-12-03T10:00:00.000Z"
};

//make the request to Graph
try{
	let res = await client.api('/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions')
		.version('beta')
		.post({extension : extensions});
	console.log(res);
} catch (error) {
	throw error;
}

```