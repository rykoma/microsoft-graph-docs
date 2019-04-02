
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const buckets = {
  name: "Development"
};

//make the request to Graph
try{
	let res = await client.api('/planner/buckets/{bucket-id}')
		.update({plannerBucket : buckets});
	console.log(res);
} catch (error) {
	throw error;
}

```