
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const add = {
  address: "Sheet1!A1:D5",
  hasHeaders: true
};

let res = await client.api('/me/drive/items/{id}/workbook/tables/add')
	.post({String : add});

```