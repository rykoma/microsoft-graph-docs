
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tasks = {
  planId: "xqQg5FS2LkCp935s-FIFm2QAFkHM",
  bucketId: "hsOf2dhOJkqyYYZEtdzDe2QAIUCR",
  title: "Update client list",
  assignments: {
    fbab97d0-4932-4511-b675-204639209557: {
      @odata.type: "#microsoft.graph.plannerAssignment",
      orderHint: " !"
    }
  },
};

//make the request to Graph
try{
	let res = await client.api('/planner/tasks')
		.post({plannerTask : tasks});
	console.log(res);
} catch (error) {
	throw error;
}

```