
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const organization = {
  "marketingNotificationEmails" : ["marketing@contoso.com"],
  "privacyProfile" :
    {
      contactEmail:"alice@contoso.com",
      statementUrl:"https://contoso.com/privacyStatement"
    },
  "securityComplianceNotificationMails" : ["security@contoso.com"],
  "securityComplianceNotificationPhones" : ["(123) 456-7890"],
  "technicalNotificationMails" : ["tech@contoso.com"]
};

//make the request to Graph
try{
	let res = await client.api('/organization/{id}')
		.version('beta')
		.update({organization : organization});
	console.log(res);
} catch (error) {
	throw error;
}

```