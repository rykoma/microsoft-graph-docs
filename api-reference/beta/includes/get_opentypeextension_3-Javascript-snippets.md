
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')')
	.version('beta')
	.filter('id eq 'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')')
	.expand('extensions')
	.get();

```