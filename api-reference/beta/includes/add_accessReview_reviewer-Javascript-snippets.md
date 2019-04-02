
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const reviewers = {
    id:"006111db-0810-4494-a6df-904d368bd81b"
}
;

//make the request to Graph
try{
	let res = await client.api('/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/reviewers')
		.version('beta')
		.post({accessReviewReviewer : reviewers});
	console.log(res);
} catch (error) {
	throw error;
}

```