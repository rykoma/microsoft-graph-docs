
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const forward = {
  comment: "comment-value",
  toRecipients: [
    {
      emailAddress: {
        name: "name-value",
        address: "address-value"
      }
    }
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/groups/{id}/threads/{id}/posts/{id}/forward')
		.post({String : forward});
	console.log(res);
} catch (error) {
	throw error;
}

```