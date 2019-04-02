
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const fields = {
    Color: "Fuchsia",
    Quantity: 934
};

//make the request to Graph
try{
	let res = await client.api('/sites/{site-id}/lists/{list-id}/items/{item-id}/fields')
		.update({fieldValueSet : fields});
	console.log(res);
} catch (error) {
	throw error;
}

```