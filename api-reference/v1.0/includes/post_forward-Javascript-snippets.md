
```Javascript

const options = {
	authProvider,
};

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
};

let res = await client.api('/groups/{id}/threads/{id}/posts/{id}/forward')
	.post({String : forward});

```