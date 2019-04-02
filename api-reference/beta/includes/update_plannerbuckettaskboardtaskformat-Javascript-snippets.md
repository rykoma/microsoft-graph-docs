
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const bucketTaskBoardFormat = {
  orderHint: "A6673H Ejkl!"
};

//make the request to Graph
try{
	let res = await client.api('/planner/tasks/hsOf2dhOJkqyYYZEtdzDe2QAIUCR/bucketTaskBoardFormat')
		.version('beta')
		.update({plannerBucketTaskBoardTaskFormat : bucketTaskBoardFormat});
	console.log(res);
} catch (error) {
	throw error;
}

```