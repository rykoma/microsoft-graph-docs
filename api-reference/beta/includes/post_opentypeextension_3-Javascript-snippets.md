
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const extensions = {
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "extensionName" : "Com.Contoso.Deal",
  "companyName" : "Alpine Skis",
  "dealValue" : 1010100,
  "expirationDate" : "2015-07-03T13:04:00.000Z"
}
;

//make the request to Graph
try{
	let res = await client.api('/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl17IsAAA=')/extensions')
		.version('beta')
		.post({extension : extensions});
	console.log(res);
} catch (error) {
	throw error;
}

```