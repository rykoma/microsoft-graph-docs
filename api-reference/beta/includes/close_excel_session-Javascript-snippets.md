
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const closeSession = {

};

let res = await client.api('/me/drive/items/{id}/workbook/closeSession')
	.version('beta')
	.post({workbook : closeSession});

```