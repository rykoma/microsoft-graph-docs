
```Javascript

const options{
	authProvider,
};

//initialise the client
const client = Client.init(options);

const schedulingGroups = {
  displayName: "Cashiers",
  isActive: true,
  userIds: [
    "c5d0c76b-80c4-481c-be50-923cd8d680a1",
    "2a4296b3-a28a-44ba-bc66-0274b9b95851"
  ]
}
;

//make the request to Graph
try{
	let res = await client.api('/teams/{teamId}/schedule/schedulingGroups')
		.version('beta')
		.post({schedulingGroup : schedulingGroups});
	console.log(res);
} catch (error) {
	throw error;
}

```