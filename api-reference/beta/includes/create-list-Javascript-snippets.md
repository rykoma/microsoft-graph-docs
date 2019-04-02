
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const lists = {
  name: "Books",
  columns: [
    {
      name: "Author",
      text: { }
    },
    {
      name: "PageCount",
      number: { }
    }
  ],
  list: {
    template: "genericList"
  }
};

//make the request to Graph
try{
	let res = await client.api('/sites/{site-id}/lists')
		.version('beta')
		.post({list : lists});
	console.log(res);
} catch (error) {
	throw error;
}

```