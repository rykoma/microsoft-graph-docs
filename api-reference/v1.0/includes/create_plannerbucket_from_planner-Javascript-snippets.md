
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const buckets = {
  name: "Advertising",
  planId: "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  orderHint: " !"
}
;

//make the request to Graph
try{
	let res = await client.api('/planner/buckets')
		.post({plannerBucket : buckets});
	console.log(res);
} catch (error) {
	throw error;
}

```