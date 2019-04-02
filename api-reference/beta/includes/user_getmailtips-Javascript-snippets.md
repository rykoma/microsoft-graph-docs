
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const getMailTips = {
    EmailAddresses: [
        "danas@contoso.onmicrosoft.com", 
        "fannyd@contoso.onmicrosoft.com"
    ],
    MailTipsOptions: "automaticReplies, mailboxFullStatus"
}
;

//make the request to Graph
try{
	let res = await client.api('/me/getMailTips')
		.version('beta')
		.post({String : getMailTips});
	console.log(res);
} catch (error) {
	throw error;
}

```