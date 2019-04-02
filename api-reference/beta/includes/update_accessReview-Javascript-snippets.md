
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const accessReviews = {
    displayName:"TestReview new name"
};

//make the request to Graph
try{
	let res = await client.api('/accessReviews('006111db-0810-4494-a6df-904d368bd81b')')
		.version('beta')
		.update({accessReview : accessReviews});
	console.log(res);
} catch (error) {
	throw error;
}

```