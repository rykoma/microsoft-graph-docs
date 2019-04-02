
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const messages = {
  subject: "Annual review",
  body: {
    contentType: "HTML",
    content: "You should be proud!"
  },
  toRecipients: [
    {
      emailAddress: {
        address: "rufus@contoso.com"
      }
    }
  ],
  extensions: [
    {
      @odata.type: "Microsoft.Graph.OpenTypeExtension",
      extensionName: "Com.Contoso.Referral",
      companyName: "Wingtip Toys",
      expirationDate: "2015-12-30T11:00:00.000Z",
      dealValue: 10000
    }
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/me/messages')
		.version('beta')
		.post({message : messages});
	console.log(res);
} catch (error) {
	throw error;
}

```