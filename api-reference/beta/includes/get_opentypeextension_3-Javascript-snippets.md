
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')')
		.version('beta')
		.filter('id eq 'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')')
		.expand('extensions')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```