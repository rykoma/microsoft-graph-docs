
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

//make the request to Graph
try{
	let res = await client.api('/planner/plans/2txjA-BMZEq-bKi6Wfj5aGQAB1OJ/buckets')
		.version('beta')
		.get();
	console.log(res);
} catch (error) {
	throw error;
}

```