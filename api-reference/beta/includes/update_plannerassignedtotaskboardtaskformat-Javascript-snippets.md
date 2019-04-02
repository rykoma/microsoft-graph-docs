
```Javascript

const options = {
	authProvider,
};

//initialise the client
const client = Client.init(options);

const assignedToTaskBoardFormat = {
  orderHintsByAssignee: {
    aaa27244-1db4-476a-a5cb-004607466324: "8566473P 957764Jk!"
  }
};

//make the request to Graph
try{
	let res = await client.api('/planner/tasks/01gzSlKkIUSUl6DF_EilrmQAKDhh/assignedToTaskBoardFormat')
		.version('beta')
		.update({plannerAssignedToTaskBoardTaskFormat : assignedToTaskBoardFormat});
	console.log(res);
} catch (error) {
	throw error;
}

```