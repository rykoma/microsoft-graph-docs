
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const plans = {
  title: "title-value"
};

//make the request to Graph
try{
	let res = await client.api('/planner/plans/'id'')
		.version('beta')
		.update({plannerPlan : plans});
	console.log(res);
} catch (error) {
	throw error;
}

```