
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const plans = {
  owner: "ebf3b108-5234-4e22-b93d-656d7dae5874",
  title: "title-value"
};

//make the request to Graph
try{
	let res = await client.api('/planner/plans')
		.post({plannerPlan : plans});
	console.log(res);
} catch (error) {
	throw error;
}

```