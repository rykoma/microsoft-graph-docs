
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const tasks = {
  assignments: {
    fbab97d0-4932-4511-b675-204639209557: {
      @odata.type: "#microsoft.graph.plannerAssignment",
      orderHint: "N9917 U2883!"
    }
  },
  appliedCategories: {
    category3: true,
    category4: false
  }
};

//make the request to Graph
try{
	let res = await client.api('/planner/tasks/{task-id}')
		.update({plannerTask : tasks});
	console.log(res);
} catch (error) {
	throw error;
}

```